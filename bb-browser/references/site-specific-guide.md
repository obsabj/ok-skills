# Site-specific 处理指南

## 微信公众号文章

### 提取正文

微信公众号文章的正文内容在 `#js_content` 中：

```bash
bb-browser open https://mp.weixin.qq.com/s/xxxxx
bb-browser eval "document.querySelector('#js_content').innerText"
```

### 为什么不用 snapshot？

微信公众号 DOM 很深，snapshot 输出会包含大量无关节点。直接用 `eval` 提取正文更高效。

## 知乎

### 提取回答内容

```bash
bb-browser open https://www.zhihu.com/question/xxxxx/answer/yyyyy
bb-browser eval "document.querySelector('.RichContent-inner').innerText"
```

### 提取问题标题

```bash
bb-browser eval "document.querySelector('h1').innerText"
```

## GitHub

### 查看 Issue / PR 内容

```bash
bb-browser open https://github.com/owner/repo/issues/123

# 提取主内容
bb-browser eval "document.querySelector('.comment-body').innerText"

# 或用 snapshot 操作按钮
bb-browser snapshot -i
bb-browser click @5
```

### 编辑文件

```bash
bb-browser open https://github.com/owner/repo/edit/main/README.md
bb-browser snapshot -i
# @1 [textarea]
# @2 [button] "Commit changes..."

bb-browser fill @1 "new content"
bb-browser click @2
```

## 内部系统 / 企业应用

### 复用登录态

bb-browser 运行在用户真实浏览器中，可以直接访问已登录的内部系统：

```bash
# 用户浏览器已登录企业 OA
bb-browser open https://oa.company.com/dashboard
bb-browser snapshot -i
bb-browser click @3
```

无需额外提供密码或 Cookie。

## 通用提取模式

### 提取页面主要文本

```bash
bb-browser eval "document.body.innerText.substring(0, 5000)"
```

### 提取所有链接

```bash
bb-browser eval "[...document.querySelectorAll('a')].map(a => a.href).join('\n')"
```

### 提取表格数据

```bash
bb-browser eval "
[...document.querySelectorAll('table tr')].map(tr =>
  [...tr.querySelectorAll('th,td')].map(td => td.innerText)
)
"
```

## 何时用哪种方法？

### 用 `eval` 的场景

- 提取文章正文
- 提取列表数据
- 执行自定义 DOM 查询
- 获取页面整体文本

### 用 `snapshot -i` 的场景

- 点击按钮/链接
- 填写表单
- 选择下拉框
- 勾选复选框
- 任何需要精确交互的操作

### 用 `snapshot`（完整）的场景

- 需要理解页面整体结构
- 排查为什么某个元素找不到
- 需要查看更多上下文
