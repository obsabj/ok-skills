# OK Skills

简体中文 | [English](README.md)

面向 pi coding agent / Codex / Claude Code 等 agents 的技能集合。

## 仓库包含内容

- 按目录组织的可复用技能（`<skill-name>/SKILL.md`）。
- 部分上游 skill 包会放在命名空间目录下（例如 `impeccable/`）。
- 技能所需的可选参考资料、脚本、许可证文件。
- 中英文双语概览文档（`README.md` + `README.zh-CN.md`）。

## 快速开始

1. 克隆本仓库。
2. 将需要的技能目录复制到本地技能目录（例如：`~/.codex/skills` 或 `~/.agents/skills`）。
3. 在项目说明文件（如 `AGENTS.md`）中定义技能触发条件。
4. 通过技能名显式调用，或自然描述需求让 agent 自动匹配技能。

本仓库无需构建即可使用。

## 技能列表

| 技能                                                                | 说明                                                                |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [agent-browser](agent-browser/SKILL.md)                             | 自动化浏览器操作，用于网页测试、表单填写、截图与数据提取。          |
| [ai-elements](ai-elements/SKILL.md)                                 | 为 ai-elements 组件库创建新的 AI 聊天界面组件，遵循可组合模式与 shadcn/ui 约定。 |
| [brainstorming](brainstorming/SKILL.md)                             | 在任何创造性工作前使用，用于澄清意图、需求与设计。                  |
| [ctx7-cli](ctx7-cli/SKILL.md)                                       | 使用官方 Context7 CLI 完成文档查询、skills 管理和 MCP 配置。        |
| [dogfood](dogfood/SKILL.md)                                         | 系统化测试 Web 应用并产出可复现的问题报告，附步骤截图与录屏证据。   |
| [electron](electron/SKILL.md)                                       | 通过 agent-browser + Chrome DevTools Protocol（CDP）自动化 Electron 桌面应用。 |
| [exa-search](exa-search/SKILL.md)                                   | 使用 Exa 进行网页/代码/公司调研，含参数与示例；需要联网搜索时使用。 |
| [find-skills](find-skills/SKILL.md)                                 | 当用户需要特定能力时，用于发现和安装现成技能。                      |
| [get-api-docs](get-api-docs/SKILL.md)                               | 在编写第三方 API 或 SDK 相关代码前，用 `chub` 拉取当前文档再继续。 |
| [gh-address-comments](gh-address-comments/SKILL.md)                 | 使用 gh CLI 处理当前分支 PR 的评审/issue 评论，并先验证登录状态。   |
| [gh-fix-ci](gh-fix-ci/SKILL.md)                                     | 检查 GitHub Actions 失败项，提取日志并制定修复方案。                |
| [pdf](pdf/SKILL.md)                                                 | 处理 PDF 的读取、生成与审查，强调渲染后的视觉检查和 Python PDF 工具链。 |
| [planning-with-files](planning-with-files/SKILL.md)                 | 面向复杂任务的文件化规划（task_plan/findings/progress）。           |
| [prompt-engineering-patterns](prompt-engineering-patterns/SKILL.md) | 高级提示工程方法，提升生产环境的可靠性与可控性。                    |
| [remotion-best-practices](remotion-best-practices/SKILL.md)         | Remotion 最佳实践：在 React 中创建视频。                           |
| [skill-creator](skill-creator/SKILL.md)                             | 创建或更新技能，聚焦专业知识、工作流与工具集成。                    |
| [design-taste-frontend](design-taste-frontend/SKILL.md)             | 面向高质量前端界面设计的 UI/UX 工程技能，强调有意图的视觉与实现。   |
| [adapt](impeccable/adapt/SKILL.md)                                  | 让设计适配不同屏幕尺寸、设备、上下文或平台，确保跨环境体验一致。    |
| [animate](impeccable/animate/SKILL.md)                              | 审视某个功能，并用有目的的动画、微交互和动效增强可用性与愉悦感。    |
| [audit](impeccable/audit/SKILL.md)                                  | 全面审计界面质量，覆盖可访问性、性能、主题与响应式设计，并输出带严重级别与建议的详细报告。 |
| [bolder](impeccable/bolder/SKILL.md)                                | 强化过于安全或平淡的设计，让它更有视觉张力，同时保持可用性。        |
| [clarify](impeccable/clarify/SKILL.md)                              | 改善不清晰的 UX 文案、错误信息、微文案、标签与说明，让界面更易理解和使用。 |
| [colorize](impeccable/colorize/SKILL.md)                            | 为过于单色或缺乏趣味的功能加入有策略的色彩，让界面更有表现力和吸引力。 |
| [critique](impeccable/critique/SKILL.md)                            | 从 UX 视角评估设计效果，审视视觉层级、信息架构、情绪表达和整体质量，并给出可执行反馈。 |
| [delight](impeccable/delight/SKILL.md)                              | 加入愉悦、个性和意外之喜，让界面更难忘、更好用，把“可用”提升到“令人喜欢”。 |
| [distill](impeccable/distill/SKILL.md)                              | 移除不必要的复杂度，把设计提炼到本质。好设计应当简洁、有力、干净。   |
| [extract](impeccable/extract/SKILL.md)                              | 抽取并整合可复用组件、设计 tokens 和模式进入设计系统，丰富组件库并提升系统化复用。 |
| [frontend-design](impeccable/frontend-design/SKILL.md)              | 创建有辨识度、生产级的高质量前端界面，适用于构建 Web 组件、页面、artifact、海报或应用。 |
| [harden](impeccable/harden/SKILL.md)                                | 通过更好的错误处理、i18n、文本溢出和边界情况处理，提升界面韧性，使其更稳健、更适合生产。 |
| [normalize](impeccable/normalize/SKILL.md)                          | 将设计规范化到你的设计系统并确保一致性。                            |
| [onboard](impeccable/onboard/SKILL.md)                              | 设计或改进引导流程、空状态和首次使用体验，帮助用户更快上手并理解价值。 |
| [optimize](impeccable/optimize/SKILL.md)                            | 优化界面性能，包括加载速度、渲染、动画、图片和包体积，让体验更快更顺滑。 |
| [polish](impeccable/polish/SKILL.md)                                | 上线前的最终质量打磨，修复对齐、间距、一致性和细节问题，把“不错”提升到“出色”。 |
| [quieter](impeccable/quieter/SKILL.md)                              | 降低过于张扬或视觉攻击性强的设计强度，在保持影响力的同时减少噪音。   |
| [teach-impeccable](impeccable/teach-impeccable/SKILL.md)            | 一次性收集项目的设计上下文并保存到 AI 配置文件中，建立持久的设计指南。 |
| [test-driven-development](test-driven-development/SKILL.md)         | TDD 流程指引：任何功能或修复先写测试。                              |
| [vercel-react-best-practices](vercel-react-best-practices/SKILL.md) | 来自 Vercel Engineering 的 React / Next.js 性能优化实践，适用于编写、审查和重构前端代码。 |
| [xlsx](xlsx/SKILL.md)                                               | 覆盖表格创建、编辑与分析，支持公式、格式和可视化图表。              |

`frontend-design` 及其关联设计命令技能（`adapt` 到 `teach-impeccable`）以 `impeccable/` 目录形式收录，来源于 [`pbakaus/impeccable`](https://github.com/pbakaus/impeccable) 的提交 `0df1ba59dc80b8b1891ee42eed0ef4e03d7ef165`。来源归属保存在 `impeccable/NOTICE.md`。

## 目录结构

```text
ok-skills/
  README.md
  README.zh-CN.md
  <skill-name>/
    SKILL.md
    references / scripts / examples（可选）
  impeccable/
    README.md
    LICENSE
    NOTICE.md
    <skill-name>/
      SKILL.md
      reference（可选）
```

## 贡献指南

欢迎为现有技能改进或新增技能。

1. 触发条件要明确且可验证。
2. 示例尽量简洁，强调可执行性。
3. 若依赖外部工具，请在 `SKILL.md` 中明确标注依赖。

## 许可证

本仓库主许可证见 [LICENSE](LICENSE)。
部分技能目录可能包含额外许可证或归属声明文件（例如 `xlsx/`、`skill-creator/`、`impeccable/`）。
