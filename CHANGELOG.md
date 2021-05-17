# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
as well as the [Conventional Commits](https://www.conventionalcommits.org) 
specification.

## Unreleased

* Nothing

## [2.1.0] 2021-05-17

### Added

* Parameter `used_shell` to set the file to be sourced.

### Changed

* Don't run execution of keychain in the background. This can lead to errors in
  the following source in case the keychain execution is too slow.
* Switch to handler where possible.

## [2.0.0] 2021-05-15

### Added

* New parameter `keychain_args`.

### Changed

* **BREAKING CHANGE**: Switched default of `login_file` from `~/.bash_profile`
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
