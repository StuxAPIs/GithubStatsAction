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

Releases follow [Semantic Versioning](https://semver.org/):

1. Update [CHANGELOG.md](CHANGELOG.md) with what changed.
2. Bump [VERSION.md](VERSION.md).
3. Run `commit.sh` (or `commit.bat` on Windows) to commit and tag the release.

## Questions

Reach out at [hello@stuxapis.net](mailto:hello@stuxapis.net).
