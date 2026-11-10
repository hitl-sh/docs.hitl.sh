# CLAUDE.md

Mintlify docs for HITL (docs.hitl.sh). See README.md for layout and writing rules.

- `npx -y mint@latest dev` to preview, `npx -y mint@latest broken-links` before committing.
- HITL is workflows-only: trigger + steps (review, AI, AI classifier, data, condition, transform, action, end); each run
  is an execution (`running`, `pending_review`, `completed`, `failed`, `timed_out`); results via
  `GET /executions/:id?wait=`, `callback_url`, or the `execution.finished` webhook. Do not document loops, loop
  requests, approval chains (410) or sessions outside `guides/moving-from-version-1.mdx`.
- API reference pages are thin wrappers over `api-reference/openapi.json`; edit the spec. Public routes are under
  `https://api.hitl.sh/v1/api/...` (plus `/v1/test` and `/v1/upload/*`).
- Use real response bodies for examples, production hosts only, example.com people only.
- Images: `images/<section>/`, under 400 KB, inside `<Frame>` with alt text. Delete images no page uses.
- Removed pages get a redirect in `docs.json`.
