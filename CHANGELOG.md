# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
as well as the [Conventional Commits](https://www.conventionalcommits.org) 
specification.

## Unreleased

* Nothing

## [5.0.2] 2021-05-19

### Fixed

* Missing import of `assert.yml`.

## [5.0.1] 2021-05-19

### Fixed

* Indent `galaxy_tags` tag leading to error.

## [5.0.0] 2021-05-19

### Added

* More supported platforms and versions.

### Changed

* **BREAKING CHANGE**: Prefix all variables with `keychain_`.

## [4.0.0] 2021-05-19

### Added

* Support for other OS systems by switching from apt to package module.

### Changed

* **BREAKING CHANGE**: Removed `absent` feature.

## [3.0.1] 2021-05-18

### Changed

* Removed empty exceptions file.

## [3.0.0] 2021-05-18

### Added

* Asserts that test all required variables.

### Changed

* Reworked README.
* Changed license.
* Changed overall formatting.

## [2.1.0] 2021-05-17

### Added

* Parameter `keychain_used_shell` to set the file to be sourced.

### Changed

* Don't run execution of keychain in the background. This can lead to errors in
  the following source in case the keychain execution is too slow.
* Switch to handler where possible.

## [2.0.0] 2021-05-15

### Added

* New parameter `keychain_args`.

### Changed

* **BREAKING CHANGE**: Switched default of `keychain_login_file` from `~/.bash_profile`
  to `~/.profile`.
* **BREAKING CHANGE**: Removed `timeout_minutes`. Replaced with `keychain_args`.

## [1.0.2] 2021-05-15 

### Changed

* Small improvements and fixes around CI and docs.

## [1.0.1] 2021-05-15 

### Added

* GitHub workflow that creates a GitHub release.

## [1.0.0] 2021-05-15 

* Intial release.

## Unreleased

* Nothing
