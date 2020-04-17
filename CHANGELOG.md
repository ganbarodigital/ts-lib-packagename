# CHANGELOG

## Introduction

This CHANGELOG tells you:

* when a release was made
* what is in each release

It also tells you what changes have been completed, and will be included in the next tagged release.

For each release, changes are grouped under these headings:

* _Backwards-Compatibility Breaks_: a list of any backwards-compatibility breaks
* _New_: a list of new features. If the feature came from a contributor via a PR, make sure you link to the PR and give them a mention here.
* _Fixes_: a list of bugs that have been fixed. If there's an issue for the bug, make sure you link to the GitHub issue here.
* _Dependencies_: a list of dependencies that have been added / updated / removed.
* _Tools_: a list of bundled tools that have been added / updated / removed.

## develop branch

The following changes have been completed, and will be included in the next tagged release.

### Tools

* Upgraded the 'scripts' section in `package.json` to the latest standard.

## v0.3.0

Released Friday, 17th April 2020.

### Dependencies

* Upgraded to v0.3 of `@ganbarodigital/ts-lib-error-reporting'

## v0.2.4

Released Monday, 6th April 2020.

### Dependencies

* Upgraded everything to fix a vulnerability in `minimist`
* Moved TypeScript et al into the `devDependencies` section

## v0.2.3

Released Thursday, 20th February 2020.

### Refactor

* We now republish internal types/functions from `ts-lib-error-reporting`
  - addresses ongoing circular dependency problems
  - ensures we never get out-of-sync with the definitions in `ts-lib-error-reporting`

## v0.2.2

Released Thursday, 20th February 2020.

### Dependencies

* Added explicit dep on `ts-lib-http-types`
  - needed after upstream changes to `ts-lib-error-reporting`

## v0.2.1

Released Thursday, 20th February 2020.

### Dependencies

* Updated to latest release of `ts-lib-error-reporting`.

## v0.2.0

Released Thursday, 20th February 2020.

### Backwards-Compatibility Breaks

* All error handling has been switched over to the `@ganbarodigital/ts-lib-error-reporting` library.

## v0.1.0

Released Sunday, 2nd February 2020.

### New

* Added `PackageName` type.
* Added `isPackageNameData()` data guard.
* Added `mustBePackageNameData()` data guarantee.
* Added `packageNameFrom()` smart constructor.
