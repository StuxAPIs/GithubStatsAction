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

## Releases

Releases follow [Semantic Versioning](https://semver.org/):

1. Update [CHANGELOG.md](CHANGELOG.md) with what changed.
2. Bump [VERSION.md](VERSION.md).
3. Run `commit.sh` (or `commit.bat` on Windows) to commit and tag the release.

## Questions

Reach out at [contact@stuxapis.net](mailto:contact@stuxapis.net).
