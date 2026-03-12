# OK Skills

English | [简体中文](README.zh-CN.md)

A curated collection of skills for the pi coding agent / Codex / Claude Code and other agents.

## What This Repo Includes

- Ready-to-use skills under separate folders (`<skill-name>/SKILL.md`).
- Some imported upstream skill packs are namespaced under a vendor folder (for example `impeccable/`).
- Optional references/scripts/licenses bundled with individual skills when needed.
- A bilingual overview (`README.md` + `README.zh-CN.md`).

## Quick Start

1. Clone this repository.
2. Copy the skill folders you need into your local skill directory (for example: `~/.codex/skills` or `~/.agents/skills`).
3. In your project instructions (such as `AGENTS.md`), define when each skill should be triggered.
4. Invoke by name or ask naturally; the agent can pick matching skills based on intent.

No build step is required.

## Skills

| Skill                                                               | Description                                                                                     |
| ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [agent-browser](agent-browser/SKILL.md)                             | Automates browser interactions for web testing, form filling, screenshots, and data extraction. |
| [ai-elements](ai-elements/SKILL.md)                                 | Create new AI chat interface components for the ai-elements library with composable patterns and shadcn/ui conventions. |
| [brainstorming](brainstorming/SKILL.md)                             | Use before any creative work to clarify intent, requirements, and design.                       |
| [ctx7-cli](ctx7-cli/SKILL.md)                                       | Use the official Context7 CLI for docs lookup, skill management, and MCP setup.                 |
| [dogfood](dogfood/SKILL.md)                                         | Systematically test web apps and deliver reproducible issue reports with screenshots/videos.     |
| [electron](electron/SKILL.md)                                       | Automate Electron desktop apps via agent-browser and Chrome DevTools Protocol (CDP).            |
| [exa-search](exa-search/SKILL.md)                                   | Use Exa for web/code/company research with parameters and examples; for online search.          |
| [find-skills](find-skills/SKILL.md)                                 | Discover and install existing skills when users ask for specialized capabilities.               |
| [get-api-docs](get-api-docs/SKILL.md)                               | Fetch current third-party API or SDK docs with `chub` before writing code against them.         |
| [gh-address-comments](gh-address-comments/SKILL.md)                 | Address PR review/issue comments with gh CLI after verifying auth.                              |
| [gh-fix-ci](gh-fix-ci/SKILL.md)                                     | Inspect failing GitHub Actions checks, summarize logs, and plan fixes.                          |
| [pdf](pdf/SKILL.md)                                                 | Read, create, and review PDF files with visual rendering checks and Python PDF tooling.         |
| [planning-with-files](planning-with-files/SKILL.md)                 | File-based planning for complex tasks using task_plan/findings/progress.                        |
| [prompt-engineering-patterns](prompt-engineering-patterns/SKILL.md) | Advanced prompt engineering patterns for reliable, production LLMs.                             |
| [remotion-best-practices](remotion-best-practices/SKILL.md)         | Best practices for Remotion - Video creation in React.                                       |
| [skill-creator](skill-creator/SKILL.md)                             | Guide for creating or updating skills with specialized knowledge, workflows, and tool integrations. |
| [design-taste-frontend](design-taste-frontend/SKILL.md)             | Senior UI/UX engineering skill for intentional, high-quality frontend design decisions.         |
| [adapt](impeccable/adapt/SKILL.md)                                  | Adapt designs to work across different screen sizes, devices, contexts, or platforms. Ensures consistent experience across varied environments. |
| [animate](impeccable/animate/SKILL.md)                              | Review a feature and enhance it with purposeful animations, micro-interactions, and motion effects that improve usability and delight. |
| [audit](impeccable/audit/SKILL.md)                                  | Perform comprehensive audit of interface quality across accessibility, performance, theming, and responsive design. Generates detailed report of issues with severity ratings and recommendations. |
| [bolder](impeccable/bolder/SKILL.md)                                | Amplify safe or boring designs to make them more visually interesting and stimulating. Increases impact while maintaining usability. |
| [clarify](impeccable/clarify/SKILL.md)                              | Improve unclear UX copy, error messages, microcopy, labels, and instructions. Makes interfaces easier to understand and use. |
| [colorize](impeccable/colorize/SKILL.md)                            | Add strategic color to features that are too monochromatic or lack visual interest. Makes interfaces more engaging and expressive. |
| [critique](impeccable/critique/SKILL.md)                            | Evaluate design effectiveness from a UX perspective. Assesses visual hierarchy, information architecture, emotional resonance, and overall design quality with actionable feedback. |
| [delight](impeccable/delight/SKILL.md)                              | Add moments of joy, personality, and unexpected touches that make interfaces memorable and enjoyable to use. Elevates functional to delightful. |
| [distill](impeccable/distill/SKILL.md)                              | Strip designs to their essence by removing unnecessary complexity. Great design is simple, powerful, and clean. |
| [extract](impeccable/extract/SKILL.md)                              | Extract and consolidate reusable components, design tokens, and patterns into your design system. Identifies opportunities for systematic reuse and enriches your component library. |
| [frontend-design](impeccable/frontend-design/SKILL.md)              | Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications. |
| [harden](impeccable/harden/SKILL.md)                                | Improve interface resilience through better error handling, i18n support, text overflow handling, and edge case management. Makes interfaces robust and production-ready. |
| [normalize](impeccable/normalize/SKILL.md)                          | Normalize design to match your design system and ensure consistency.                           |
| [onboard](impeccable/onboard/SKILL.md)                              | Design or improve onboarding flows, empty states, and first-time user experiences. Helps users get started successfully and understand value quickly. |
| [optimize](impeccable/optimize/SKILL.md)                            | Improve interface performance across loading speed, rendering, animations, images, and bundle size. Makes experiences faster and smoother. |
| [polish](impeccable/polish/SKILL.md)                                | Final quality pass before shipping. Fixes alignment, spacing, consistency, and detail issues that separate good from great. |
| [quieter](impeccable/quieter/SKILL.md)                              | Tone down overly bold or visually aggressive designs. Reduces intensity while maintaining design quality and impact. |
| [teach-impeccable](impeccable/teach-impeccable/SKILL.md)            | One-time setup that gathers design context for your project and saves it to your AI config file. Run once to establish persistent design guidelines. |
| [test-driven-development](test-driven-development/SKILL.md)         | TDD workflow: write tests first for any feature or fix.                                         |
| [vercel-react-best-practices](vercel-react-best-practices/SKILL.md) | React and Next.js performance optimization guidelines from Vercel Engineering for writing, reviewing, and refactoring frontend code. |
| [xlsx](xlsx/SKILL.md)                                               | Comprehensive spreadsheet creation, editing, and analysis with formulas, formatting, and charts.|

The `frontend-design` and related design command skills (`adapt` through `teach-impeccable`) are vendored under `impeccable/` from [`pbakaus/impeccable`](https://github.com/pbakaus/impeccable) at commit `0df1ba59dc80b8b1891ee42eed0ef4e03d7ef165`. Attribution is preserved in `impeccable/NOTICE.md`.

## Structure

```text
ok-skills/
  README.md
  README.zh-CN.md
  <skill-name>/
    SKILL.md
    references / scripts / examples (optional)
  impeccable/
    README.md
    LICENSE
    NOTICE.md
    <skill-name>/
      SKILL.md
      reference (optional)
```

## Contributing

Contributions are welcome for new skills or improvements to existing ones.

1. Keep trigger conditions explicit and testable.
2. Keep examples concise and execution-oriented.
3. If a skill depends on external tools, document that dependency in `SKILL.md`.

## License

This repository is licensed under [LICENSE](LICENSE).
Some skills may include additional license files or notices for skill-specific assets and attribution (for example under `xlsx/`, `skill-creator/`, and `impeccable/`).
