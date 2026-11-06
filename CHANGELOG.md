# Changelog

All notable changes to stuxdesign.github.io are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.11.06-1

### Added

- `.github/workflows/ci.yml`, which runs `bash tests/version.sh` on pushes to `main` and `test` and on pull requests into `main`, so the pull request from `test` has a check to pass.

### Changed

- README (Versioning) and CONTRIBUTING (a new Branches section) say work happens on `test`, reaches `main` only through a pull request that needs CI to pass and is reviewed and merged by Leo, and that releases are committed and tagged on `test`. The commit scripts' push hint says `test`.

## v26.11.06

### Changed

- The README describes what this repo actually is, the redirect from stuxdesign.github.io to
  github.com/StuxDesign, instead of a generic "redirect to example.com" template (it isn't a template repo).
- The README and CONTRIBUTING use the light/dark Stux.Design logo and the full name **Stux.Design GitHub Pages
  Redirect**.
- The README's licence section reads © Stux.Group (it said "Feel free to use this template"), with the standard
  Stux.Design footer.

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.0
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## v1.0.0

### Added
- Initial GitHub Pages redirect repo for Stux.Design, redirecting `stuxdesign.github.io` to `github.com/StuxDesign`, deployed through GitHub Actions (`.github/workflows/pages.yml`) — `VERSION.md`/`CHANGELOG.md`/`CONTRIBUTING.md`/`commit.sh`+`commit.bat`/`.gitignore` added, following the standard release-flow convention used across other Stux.Group family repos.
