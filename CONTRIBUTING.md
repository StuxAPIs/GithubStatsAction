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

## Branches

- Work on `test`, or on a branch off it. Never push to `main`
- Changes reach `main` only through a pull request from `test` into `main`, which needs CI to pass and is reviewed and merged by Leo
- Release commits and tags are made on `test` (`git push origin test --tags`) and take effect when the pull request is merged. Workflows pin its tags in `uses:`, so a release is usable once it is merged.

## Releases

Releases use [Date Versioning](https://datevers.ing) (since v26.11.07; v3.0.0 to v3.0.8 were SemVer, and it never goes back):

1. Add a `## vYY.MM.DD` entry at the top of [CHANGELOG.md](CHANGELOG.md), with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set [VERSION.md](VERSION.md) to the same bare version: today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Set `package.json`'s version to its SemVer form (`26.11.07` → `26.11.0700`, `26.11.07-1` → `26.11.0701`).
3. Run `bash tests/version.sh`.
4. Run `commit.sh` (or `commit.bat` on Windows) to commit and tag the release. It never pushes.

When the tag reaches GitHub, `update-tags.yml` moves the floating tags to it: `v3` (kept for workflows that pinned the last SemVer major), the year (`v26`) and the month (`v26.11`).

## Questions

Reach out at [hello@stuxapis.net](mailto:hello@stuxapis.net).
