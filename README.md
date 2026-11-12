# cherrylove-mobile

Expo / React Native app for partners.

Part of **CherryLove**, a private shared space for a couple. This repo holds no product code yet: the first code
comes from step 1 of its implementation plan.

## Source of truth

All requirements, decisions and architecture live in
[cherryLove-docs](https://github.com/cmlooz/cherryLove-docs/blob/main/README.md). The rules for this repo come from: ADR-002 §4 (layout), ADR-004 (secure store), ADR-007 (HEIC to JPEG), ADR-012 (i18n), ADR-013 §4 (Expo push), ADR-016 (Expo SDK 58).

## Working agreement

- Conventional Commits, 1 commit per step, 1 PR per phase, ≥ 1 test per step (DEC-023).
- Every commit, PR and test cites the REQ / DEC / ADR IDs it implements.
- `main` is protected: PR + green `ci`, rebase merge only (ADR-015, DEC-039).
- Enable the local hook once per clone: `git config core.hooksPath .githooks`.
