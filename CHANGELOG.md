# Changelog

All notable changes made in the StuxAPIs fork of GitHub Readme Stats Action
are documented here, tracking this fork independently of upstream's own
release history. For upstream history, see
[stats-organization/github-readme-stats-action](https://github.com/stats-organization/github-readme-stats-action).

Since v26.11.07 this project uses [Date Versioning](https://datevers.ing) (`YY.MM.DD`, the UTC release
date, with `-1`, `-2`… for later releases the same day). v3.0.0 to v3.0.8 used Semantic Versioning (they
started at v3.0.0 because this fork's history carries upstream's own tags up to v2.0.2). The `v3` tag still
follows the latest release, so workflows using `@v3` keep getting updates.

## v26.11.07

### Changed

- **Date Versioning.** This is the first release numbered by its UTC release date (`YY.MM.DD`, then `-1`, `-2`… the same day) instead of Semantic Versioning, and every release after it is too. Date Versions sort above every `v3.x.y` tag
- Nothing changes for workflows: `@v3` still moves to every new release, as before. Each release also moves `v26` (the year) and `v26.11` (the month), so `@v26` follows this year's releases, and `@v26.11.07` pins this one
- `.github/workflows/update-tags.yml` moves those tags itself on every Date Version tag push, instead of `haya14busa/action-update-semver` (which only understands SemVer)
- `commit.sh` and `commit.bat` accept only a real, non-future Date Version, and `tests/version.sh` (run in CI) checks `VERSION.md` and the changelog
- README examples pin `@v26.11.07`, and the README, CONTRIBUTING and this intro describe Date Versioning
- `package.json`'s version is the Date Version's SemVer form (`26.11.0700`)

## v3.0.8

### Changed

- CI (`.github/workflows/ci.yml`) also runs on pushes to `test`
- `commit.sh` and `commit.bat` end by saying to push `test` and open a pull request into `main`
- README (Versioning) and CONTRIBUTING (a new Branches section) describe the `test` branch flow: work and releases happen on `test`, and reach `main` only through a reviewed pull request that needs CI to pass

## v3.0.7

### Changed

- The logos and icons in the Markdown docs (README and the like) follow GitHub's light or dark theme, using each brand's `logo-light`/`logo-dark` and `icon-light`/`icon-dark` files

## v3.0.6

### Fixed
- `README.md`'s Stux.Group brand icon URL had a leftover duplicated `/global/` path segment (`global.media.stux.group/global/icon.png`) — corrected to `https://global.media.stux.group/icon.png`

## v3.0.5

### Changed
- `CONTRIBUTING.md`'s general contact address changed from `contact@stuxapis.net` to `hello@stuxapis.net`, matching the convention used across other StuxAPIs repos

## v3.0.4

### Changed
- `README.md`'s header logo now shows StuxAPIs' own logo (`https://global.media.stuxapis.net/logo.png`) instead of the generic Stux.Group fallback, and the footer "Built & Maintained by StuxAPIs" icon now uses StuxAPIs' own icon instead of the GitHub org avatar — now that StuxAPIs has real branding of its own, more specific than the org-wide Stux.Group fallback

## v3.0.3

### Changed
- `README.md`'s "Powered by StuxAPIs" line replaced with "Built & Maintained by StuxAPIs, Hosted by Stuxedo" (both linked, to `github.com/StuxAPIs` and `stuxedo.com`), matching the branding used everywhere else in the org

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
