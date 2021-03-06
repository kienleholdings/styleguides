# Base TSConfig

> Kienle Holdings Base TSConfig

## Installation

1. Install peer dependencies: `yarn add typescript -D`
1. Install config `yarn add @kienleholdings/base-tsconfig`

## Usage

1. Create a file named `tsconfig.json`
1. Add the following:

```JSON
{
  "extends": "@kienleholdings/base-tsconfig",
}
```

## Recommended Customization

Going off by the base config is a great start, but won't get you too far. We recommend setting the
following:

- [`compilerOptions.baseUrl`](https://github.com/kienleholdings/typescript#base-url)
- [`compilerOptions.jsx`](https://github.com/kienleholdings/typescript#jsx)
- [`compilerOptions.lib`](https://github.com/kienleholdings/typescript#lib)
- [`compilerOptions.outDir`](https://github.com/kienleholdings/typescript#out-dir)
- [`compilerOptions.rootDir`](https://github.com/kienleholdings/typescript#root-dir)
- [`compilerOptions.sourceRoot`](https://github.com/kienleholdings/typescript#source-root)
- [`compilerOptions.target`](https://github.com/kienleholdings/typescript#target)
- [`compilerOptions.types`](https://github.com/kienleholdings/typescript#types)
- [`exclude`](https://github.com/kienleholdings/typescript#excluded-files)
- [`files`](https://github.com/kienleholdings/typescript#additional-typings)
- [`include`](https://github.com/kienleholdings/typescript#included-files)

A version `0.1.3` change marked `esnext` as a valid option for `compilerOptions.module` but left
`commonjs` as a default for backwards compatibility. If you're running webpack, we recommend setting
that for better tree shaking and code splitting.
