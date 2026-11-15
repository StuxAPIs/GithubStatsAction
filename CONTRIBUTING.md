# Contributing to this fork

This repository is StuxAPIs' hosted fork of
[stats-organization/github-readme-stats-action](https://github.com/stats-organization/github-readme-stats-action).

- For changes to the action's actual behaviour (`index.js`, `action.yml`,
  card generation logic), please contribute upstream first — this fork
  periodically pulls in upstream changes.
- For anything specific to how StuxAPIs hosts this fork (this fork's
  `README.md` branding or its release files), open a pull request here
  directly.

## Local setup

```bash
pnpm install
```

See the upstream README for how the action is tested and packaged.

## Branches and going live

- **`main` is what's live.** Nothing is pushed to it directly: it only changes when a pull request from `staging` is merged. Workflows pin its tags in `uses:`, so a release is usable once it is merged.
- **`staging` is the last check before live.** It only changes when a pull request from `test` is merged.
- **Work happens on `test`**, or on a branch off `test` that's merged back into it. Releases are committed and tagged on `test`; `commit.sh` / `commit.bat` refuse to run on `staging` or `main`.
- **Going live:** push `test` with its tag (`git push origin test --tags`), open a pull request into staging (`gh pr create --base staging --head test`), check staging once it's merged, then open one from staging into main (`gh pr create --base main --head staging`). Both pull requests need CI to pass and are reviewed and merged by Leo.

## Releases

Releases use [Date Versioning](https://datevers.ing) (since v26.11.07; v3.0.0 to v3.0.8 were SemVer, and it never goes back):

1. Add a `## vYY.MM.DD` entry at the top of [CHANGELOG.md](CHANGELOG.md), with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set [VERSION.md](VERSION.md) to the same bare version: today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Set `package.json`'s version to its SemVer form (`26.11.07` → `26.11.0700`, `26.11.07-1` → `26.11.0701`).
3. Run `bash tests/version.sh`.
4. Run `commit.sh` (or `commit.bat` on Windows) to commit and tag the release. It never pushes.

When the tag reaches GitHub, `update-tags.yml` moves the floating tags to it: `v3` (kept for workflows that pinned the last SemVer major), the year (`v26`) and the month (`v26.11`).

## Questions

Reach out at [hello@stuxapis.net](mailto:hello@stuxapis.net).
