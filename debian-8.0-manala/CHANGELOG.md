# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
### Changed
- Upstream update

## [2.1.0] - 2018-01-08
### Changed
- Define deb.debian.org mirror as sources
- Don't remove ISC dhcp client and dependencies

### Added
- Systemd recommends (libpam-systemd)

### Removed
- IPTables dependencies (libnfnetlink0)

## [2.0.0] - 2016-09-05
### Changed
- Use minimal bootstrap
- Permit ssh root login

### Added
- Systemd and dependencies/recommends
- Python

### Removed
- ISC dhcp client and dependencies
- Postfix and dependencies
- IPTables and dependencies
