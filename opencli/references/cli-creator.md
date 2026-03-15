# OpenCLI Adapter Guide

Use this reference when a task goes beyond running built-in `opencli` commands and requires a new site adapter.

## Workflow

1. Discover the site with `opencli explore <url> --site <name>`.
2. Probe authentication with `opencli cascade <api-url>`.
3. Choose adapter format:
   - Use YAML when the flow is mostly declarative.
   - Use TypeScript when you need interception, complex transforms, or heavier browser logic.
4. Generate or refine the adapter with `opencli synthesize <site>` or `opencli generate <url> --goal "<goal>"`.
5. Smoke-test with `opencli verify <site/name> --smoke`.

## Decision Rules

- Prefer `public` when direct HTTP works without browser state.
- Prefer `cookie` when browser `fetch(..., { credentials: 'include' })` is enough.
- Escalate to `header` when tokens or custom headers are required.
- Use `intercept` or UI-driven logic only when simpler strategies fail.

## Common Commands

```bash
opencli explore https://example.com --site mysite
opencli synthesize mysite
opencli generate https://example.com --goal "hot"
opencli cascade https://api.example.com/data
opencli verify mysite/hot --smoke
```

## Output Artifacts

Explore typically writes to `.opencli/explore/<site>/`:

- `manifest.json`: site metadata and framework hints
- `endpoints.json`: discovered endpoints and response clues
- `capabilities.json`: inferred tasks such as `hot`, `search`, or `feed`
- `auth.json`: authentication recommendations

## When To Switch From YAML To TypeScript

- You need request interception.
- You need scrolling, click-driven loading, or complex DOM coordination.
- You need more than a small amount of inline JavaScript in a declarative pipeline.

## Upstream Source

For the full upstream authoring guide, see `https://github.com/jackwener/opencli/blob/main/CLI-CREATOR.md`.
