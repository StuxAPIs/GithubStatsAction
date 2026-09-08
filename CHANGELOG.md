# Changelog

All notable changes made in the StuxAPIs fork of GitHub Readme Stats Action
are documented here, tracking this fork independently of upstream's own
release history. For upstream history, see
[stats-organization/github-readme-stats-action](https://github.com/stats-organization/github-readme-stats-action).

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Started at v3.0.0 rather than v1.0.0 — this fork's git history carries
upstream's own release tags up through v2.0.2, so anything in the v1.x/v2.x
range would collide with an existing tag.

## v3.0.2

### Changed
- `README.md`'s footer brand-attribution block updated to the new two-line format (Built & Maintained by StuxAPIs, Hosted by Stuxedo / StuxAPIs is a part of the Stux.Group brand of businesses), replacing the older single-line disclaimer

## v3.0.1

### Changed
- `README.md`'s "StuxAPIs is part of the Stux.Group Brand of Companies" line now includes the Stux.Group icon inline
- This changelog's preamble now uses the standard Keep a Changelog wording

## v3.0.0

### Added
- `VERSION.md`, `CHANGELOG.md`, `CONTRIBUTING.md`, `commit.sh`/`commit.bat` — brought the repo onto the standard StuxAPIs release flow (bump `VERSION.md`, update this changelog, run `commit.sh`/`commit.bat` to commit and tag `vX.Y.Z`)

### Changed
- `README.md` given a Stux.Group logo header and a "Powered by StuxAPIs" fork/license note
- Quick-start workflow example now references `StuxAPIs/GithubStatsAction@v3.0.0` instead of the upstream action, so copy-pasting the example actually uses this fork
