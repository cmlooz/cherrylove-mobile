# cherrylove-mobile — Claude Code instructions

Workspace rules live in `../CLAUDE.md` and `../cherryLove-docs/CLAUDE.md`; read them first.
Only `approved` documents in `../cherryLove-docs` may drive code here.

## Architecture rules for this repo

- Layout: thin Expo Router routes in `app/`; features in `src/features/`, design system in `src/ui/`, adapters in `src/platform/` (ADR-002 §4).
- Same feature vocabulary and container-presentational split as web.
- Refresh token only in expo-secure-store (ADR-004); local data in expo-sqlite through core's `LocalStore` port.
- Photos are converted from HEIC to JPEG before upload (ADR-007 §3).
- No string literals in JSX; UI in Spanish and English (DEC-021).
- Expo SDK 58 and its pinned module versions (ADR-016); native builds are decided in the production ADR.

## Always

- Strict typing, validation before `try/catch`, SOLID, official documentation first.
- 1 commit per step with ≥ 1 test citing its REQ ID; never push to `main` (open a PR).
- A gap in the docs becomes an open question in `../cherryLove-docs/02-requirements/open-questions.md`; never assume.
