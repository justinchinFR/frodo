# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.8.0] - 2022-07-11

## [0.7.1-1] - 2022-07-11

## [0.7.1-0] - 2022-07-10

## [0.7.0] - 2022-07-10

### Added

-   CHANGELOG.md
-   `conn describe` command to describe connection profiles
    -   `--show-secrets` option to `conn describe` command to show clear-text secrets
-   `--validate` option to `conn add` command to validate credentials before adding

### Changed

-   Adapted true semantic versioning
-   Pipeline changes
    -   Automated updating changelog using keep a changelog format in CHANGELOG.md
    -   Automated version bump (SemVer format) using PR comments to trigger prerelease, patch, minor, or major bumps
    -   Automated release notes extraction from CHANGELOG.md
    -   Automated GitHub release creation
    -   Renamed frodo.yml to pipeline.yml
-   Renamed connections command to `conn` with aliases `connection` and `connections` for backwards compatibility
-   Internal restructuring (#160, #135)

### Fixed

-   \#280: Fixed missing -k/--insecure param in application sub-commands #280
-   \#310: No longer storing connection profiles unless explicitly instructed to

## [0.6.4-4] - 2022-07-10 [YANKED]

## [0.6.4-3] - 2022-07-09 [YANKED]

## [0.6.4-2] - 2022-07-09 [YANKED]

## [0.6.4-1] - 2022-07-09 [YANKED]

## [0.6.4-0] - 2022-07-09 [YANKED]

## [0.6.3] - 2022-07-08 [YANKED]

## 0.6.3-alpha.1 - 0.6.3-alpha.51 [YANKED]

## 0.6.2 [YANKED]

## 0.6.1 alpha 26 - 2022-06-28

### Changed

-   Changed archive step of Windows binary build to use 7zip

## 0.6.1 alpha 22 - 0.6.1 alpha 25 [YANKED]

## 0.6.1 alpha 21 - 2022-06-27

### Added

-   Added theme delete command
-   Theme list e2e tests
-   Theme delete e2e tests
-   Added esv command
    -   esv secret - Manage secrets.
    -   esv variable - Manage variables.
    -   esv apply - Apply pending changes.
-   Updated all dependencies to the latest versions

### Changed

-   Moved secret command under new esv command

## 0.6.1 alpha 20 - 2022-06-23

### Added

-   Added journey delete command
-   journey list e2e tests
-   journey delete e2e tests

### Changed

-   Allow progressbar output to be captured in redirects

### Fixed

-   Journey import fixes
-   Journey export bug fix
-   Fix theme import issues when using /alpha or /bravo instead of alpha or bravo
-   Fix admin create-oauth2-client-with-admin-privileges command

## 0.6.1 alpha 19 - 2022-06-14

### Added

-   First stab at e2e testing of journey command
-   saml command enhancements

### Fixed

-   Detect and remove invalid tree attributes on import
-   Fixed issue where overriding deployment type would fail to detect the default realm
-   Fix theme import -A

## 0.6.1 alpha 18 - 2022-06-10

### Added

-   \--txid parameter with the logs commands to filter log output by transactionId

### Fixed

-   Bug in idm exportAllRaw

## 0.6.1 alpha 17 - 2022-06-08

### Added

-   New saml command to manage entity providers and circles of trust

### Changed

-   Updates to journey export/import commands
    -   Support for social identity providers
    -   Support for themes
    -   Support for SAML entity providers
    -   Support for SAML circles of trust
    -   Breaking changes in journey sub-commands
        -   export
            -   \-t/--tree renamed to -i/--journey-id
        -   import
            -   \-t/--tree renamed to -i/--journey-id
            -   \-i/--journey-id is now only used to select the journey to import if there are multiple journeys in the import file
            -   \-n (No re-UUID) removed
            -   new flag --re-uuid with inversed behavior of removed -n flag. Frodo by default no longer generates new UUIDs for nodes on import
-   Scalability enhancements to journey prune command. The changes allow the prune command to scale to many thousands of orphaned node configuration objects in an AM instance
-   Updated readme
-   Miscellaneous bug fixes

## 0.6.1 alpha 14 - 0.6.1 alpha 16 [YANKED]

## 0.6.1 alpha 13 - 2022-05-20

### Added

-   New script command to export and import scripts
-   New email_templates command to manage email templates
-   New application command to export and import oauth2 clients
-   New realm command to manage realms
-   New secret command to manage Identity Cloud secrets
-   New theme command to manage hosted pages UI themes
-   New admin command to perform advanced administrative tasks
-   Encrypt the password value in the connection profile
-   Added progress bars/spinners for long running operations
-   Added version option -v, --version
-   Auto provisioning of log API keys
-   Added initial unit testing

### Changed

-   Improved performance of journey command (multi-threading)
-   Consolidated settings under one folder (~/.frodo)
-   Proposed new code formatting (prettier) and style (eslint) rules
-   Updated readme
-   Update to node 18

### Fixed

-   Fixed problem with adding connection profiles
-   Miscellaneous bug fixes

[Unreleased]: https://github.com/justinchinFR/frodo/compare/v0.8.0...HEAD

[0.8.0]: https://github.com/justinchinFR/frodo/compare/v0.7.1-1...v0.8.0

[0.7.1-1]: https://github.com/rockcarver/frodo/compare/v0.7.1-0...v0.7.1-1

[0.7.1-0]: https://github.com/rockcarver/frodo/compare/v0.7.0...v0.7.1-0

[0.7.0]: https://github.com/rockcarver/frodo/compare/v0.6.4-4...v0.7.0

[0.6.4-4]: https://github.com/rockcarver/frodo/compare/v0.6.4-3...v0.6.4-4

[0.6.4-3]: https://github.com/rockcarver/frodo/compare/v0.6.4-2...v0.6.4-3

[0.6.4-2]: https://github.com/rockcarver/frodo/compare/v0.6.4-1...v0.6.4-2

[0.6.4-1]: https://github.com/rockcarver/frodo/compare/v0.6.4-0...v0.6.4-1

[0.6.4-0]: https://github.com/rockcarver/frodo/compare/v0.6.3...v0.6.4-0

[0.6.3]: https://github.com/rockcarver/frodo/compare/v0.6.3-alpha.51...v0.6.3

[0.6.3-alpha.51]: https://github.com/rockcarver/frodo/compare/6137b8b19f1c22af40af5afbf7a2e6c5a95b61cb...v0.6.3-alpha.51
