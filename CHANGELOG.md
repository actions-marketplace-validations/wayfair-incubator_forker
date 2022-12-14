# Changelog

All notable changes to `Forker` will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.6] - 2022-10-12

### Added

- A new GitHub Action `output` which allows the value of the `forkUrl` string to be accessed by subsequent steps in a GitHub Workflow.

### Changed

- Upgraded action runner config to use node v16 (support for v12 is [being deprecated](https://github.blog/changelog/2022-09-22-github-actions-all-actions-will-begin-running-on-node16-instead-of-node12/)).

## [0.0.5] - 2022-09-07

### Added

- Support for enforcing existing membership in a specified GitHub organization (see `checkUser`)
- Support for granting organization users `admin` permissions on the repository they wish to fork (see `promoteUser`)

### Changed

- Updated Jest unit tests to validate all env inputs
- Downgraded all Jest packages from v29 to v28 to resolve mismatch with `ts-jest`
- Updated README to document new inputs (`checkuser`, `promoteUser`) and remove deprecated ones (`addUser`)

### Removed

- Support for sending GitHub organization invitations to users who were not already a member (see `addUser`)

## [0.0.4] - 2022-03-23

### Added

- Numerous Dependabot dependency vulnerabilities and recommended upgrades

### Fixed

- Bug with license compliance check failing when the license format is invalid
- Edge case where Github were invited when no organization was specified

## [0.0.3] - 2022-01-11

### Added

- Missing content from Wayfair's official [OSS Template](https://github.com/wayfair-incubator/oss-template)
- Dynamic release badging system for [README](https://github.com/wayfair-incubator/forker/blob/main/README.md)
- Linting configuration for all markdown files, including local and [CI](https://github.com/wayfair-incubator/forker/actions/workflows/lint.yml)
- Several major `npm` package upgrades suggested by Dependabot

### Changed

- Improved `README` content and clarified developer instructions
- Used named constants instead of numerical response codes
- Used OSPO service account for all workflow tests
- Updated vulnerable `npm` packages to compliant versions
- Updated Dependabot configuration to search for `github-actions` updates

### Fixed

- Token access issue with actions integration tests
- Numerous `npm` and `typescript` dependency conflicts

## [0.0.2] - 2021-10-22

### Changed

- Updated all repository references to use `wayfair-incubator` organization
- Temporarily disabled actions integration tests while diagnosing a token access issue
- Resolved numerous node + typescript dependency vulnerabilities

## [0.0.1] - 2021-08-31

### Added

- Initial [release](https://github.com/wayfair-incubator/forker/releases/tag/v0.0.1) of `forker` and [publication](https://github.com/marketplace/actions/github-forker) on the Github Action marketplace
