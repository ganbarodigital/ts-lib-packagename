# PackageName Type for Typescript

## Introduction

This TypeScript micro-library provides a `PackageName` type, along with helpers for validating the data.

- [Introduction](#introduction)
- [Quick Start](#quick-start)
- [V1 API](#v1-api)
  - [PackageName](#packagename)
  - [isPackageNameData()](#ispackagenamedata)
- [NPM Scripts](#npm-scripts)
  - [npm run clean](#npm-run-clean)
  - [npm run build](#npm-run-build)
  - [npm run test](#npm-run-test)
  - [npm run cover](#npm-run-cover)

## Quick Start

```
# run this from your Terminal
npm install @ganbarodigital/ts-lib-packagename/v1
```

```typescript
// add this import to your Typescript code
import { PackageName, isPackageNameData } from "@ganbarodigital/ts-lib-packagename/v1"
```

__VS Code users:__ once you've added a single import anywhere in your project, you'll then be able to auto-import anything else that this library exports.

## V1 API

### PackageName

```typescript
/**
 * represents the name of a TypeScript package
 *
 * the package can be:
 * - any valid NPM package name
 * - and can include sub-package names too
 *
 * Sub-package names can include uppercase characters.
 *
 * examples of valid PackageNames include:
 *
 * - ts-lib-packagename
 * - @ganbarodigital/ts-lib-packagename
 * - @ganbarodigital/ts-lib-packagename/v1
 * - @ganbarodigital/ts-lib-packagename/V1/types
 *
 * Relative module names are not supported.
 *
 * At runtime, PackageName resolves to being just a `string`.
 */
export type PackageName = string & { _type: "@ganbarodigital/PackageName" };
```

`PackageName` is a _type_. (Strictly speaking, it's a _branded type_.) Use it to represent a valid TypeScript package name in type-safe code.

### isPackageNameData()

```typescript
/**
 * data guard. confirms if a proposed name for a PackageName fits
 * our legal scheme or not.
 */
export function isPackageNameData(name: string): boolean;
```

`isPackageNameData()` is a _data guard_. Use it to determine if the input string contains a valid PackageName or not.

We do not check that the named package actually exists. We only check that the name meets our naming structure.

## NPM Scripts

### npm run clean

Use `npm run clean` to delete all of the compiled code.

### npm run build

Use `npm run build` to compile the Typescript into plain Javascript. The compiled code is placed into the `lib/` folder.

`npm run build` does not compile the unit test code.

### npm run test

Use `npm run test` to compile and run the unit tests. The compiled code is placed into the `lib/` folder.

### npm run cover

Use `npm run cover` to compile the unit tests, run them, and see code coverage metrics.

Metrics are written to the terminal, and are also published as HTML into the `coverage/` folder.