# HITL documentation

Source of [docs.hitl.sh](https://docs.hitl.sh), built with [Mintlify](https://mintlify.com).

HITL (Human In The Loop) lets agents, code and automations ask people for decisions. Everything runs through
**workflows**: a trigger and steps, where a review step asks people (on iOS/Android, the web inbox at my.hitl.sh or
Telegram) and the run (an **execution**) finishes with their answer.

## Layout

| Path | What |
|---|---|
| `index.mdx`, `quickstart.mdx` | Introduction and quickstart |
| `concepts/` | Workflows, review steps, reviewers, executions |
| `guides/` | Workflow editor, webhooks, moving from HITL version 1 |
| `responses/` | Review step settings: the seven answer types and the question's content |
| `answering/` | Web inbox, mobile app, Telegram |
| `integrations/` | Agent setup prompt, MCP, CLI, REST, n8n, Zapier, Make |
| `api-reference/` | `openapi.json` (OpenAPI 3.1, server `https://api.hitl.sh/v1`) and one page per endpoint |
| `images/<section>/` | Screenshots, under 400 KB each |
| `images/readme/` | Images for the npm READMEs of `@hitl-sh/cli`, `@hitl-sh/mcp`, `@hitl-sh/core` and `n8n-nodes-human-in-the-loop`, linked from npm as `https://docs.hitl.sh/images/readme/...`. No page uses them; keep them. Those READMEs also link `images/mcp/*`, `images/n8n/*` and `images/mobile/boolean.png` |
| `docs.json` | Navigation, redirects for removed pages, theme |

## Run locally

```bash
npx -y mint@latest dev            # http://localhost:3000
npx -y mint@latest broken-links   # must be clean before merging
```

## Writing rules

- Workflows only. Loops, loop requests, approval chains and sessions are retired; only
  `guides/moving-from-version-1.mdx` mentions them.
- Examples are real API responses (demo data: Jordan Lee, Priya Shah, Marcus Webb, Elena Garcia, Sam Okafor at
  example.com). Every URL points at production (`api.hitl.sh`, `my.hitl.sh`); never show dev hosts, real emails or keys.
- Screenshots go in `<Frame>` with descriptive alt text. Compress to under 400 KB.
- Endpoint pages are generated from `api-reference/openapi.json` (`openapi: "METHOD /path"` front matter). Change the
  spec, not the page.
- Removing or renaming a page: add a redirect in `docs.json`.

Sources of truth: api.hitl.sh (`WORKFLOWS_API.md`), the CLI and MCP tools in `hitl-sh/cli`
(`packages/core/src/api-catalog.ts`), the n8n, Zapier and Make repos, and `my.hitl.sh/lib/plans.ts` for pricing.
