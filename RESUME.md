# RESUME: docs.hitl.sh

Branch: `preview` only (never main). Don't stage `.omc/` or `.next/`.

## 2026-10-29: "Moving from HITL version 1" guide (DONE, committed 7fc666a, pushed to preview 2026-10-30)

- `guides/moving-from-version-1.mdx` (written by an earlier session) replaces `guides/migration.mdx`, which contradicted the
  portal (said loops were auto-converted and invite codes stopped working). Old page removed; `/guides/migration` redirects
  to the new guide in docs.json; nav moved from Enterprise to Getting Started; approval-chains links updated.
- Fixed a broken link (`/guides/review-step` -> `/guides/workflow-designer#human-review-node`). `npx mint broken-links` passes.
- Committed only the 3 images the guide uses (`images/portal/migration-*.png`). The other 32 screenshots in `images/mobile/`
  and `images/portal/` are untracked and unused by any page.
- Open question: the guide's API section names `https://dev.api.my.hitl.sh/v1` (preview) and documents session-token
  endpoints under `/v1/mobile/migration/*`.
