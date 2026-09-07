# Changelog

All notable changes made in the StuxAPIs fork of GitHub Readme Stats Action
are documented here. Versions follow [Semantic Versioning](https://semver.org/)
(MAJOR.MINOR.PATCH) and track this fork independently of upstream's own
release history. For upstream history, see
[stats-organization/github-readme-stats-action](https://github.com/stats-organization/github-readme-stats-action).

Started at v3.0.0 rather than v1.0.0 — this fork's git history carries
upstream's own release tags up through v2.0.2, so anything in the v1.x/v2.x
range would collide with an existing tag.

## v3.0.0

### Added
- `VERSION.md`, `CHANGELOG.md`, `CONTRIBUTING.md`, `commit.sh`/`commit.bat` — brought the repo onto the standard StuxAPIs release flow (bump `VERSION.md`, update this changelog, run `commit.sh`/`commit.bat` to commit and tag `vX.Y.Z`)

### Changed
- `README.md` given a Stux.Group logo header and a "Powered by StuxAPIs" fork/license note
- Quick-start workflow example now references `StuxAPIs/GithubStatsAction@v3.0.0` instead of the upstream action, so copy-pasting the example actually uses this fork
