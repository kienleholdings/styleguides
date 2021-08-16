# Prettier Style Guide

> A Bullshit-Free Approach to Prettier

## Table of Contents

1. [Configuration File Name](#configuration-file-name)
1. [End of Line](#end-of-line)
1. [Print Width](#print-width)
1. [Prose Wrap](#prose-wrap)
1. [Single Quotes](#single-quotes)
1. [Resources](#resources)
1. [Amendments](#amendments)

## Configuration File Name

If you choose to extend our Prettier config, rather than use the `package.json` parameter, the
Prettier configuration file should be `.prettierrc` with a `.js` extension.
([`Configuration File`](https://prettier.io/docs/en/configuration.html))

> **Why?** In order to extend the Prettier config, you need to be working with a `js` file rather
> than a `json` file. The fine needs to be named `.prettierrc` otherwise Prettier won't find it and
> you may get unexpected behavior.

<!-- prettier-ignore-start -->
```markdown
<!-- Good -->
.prettierrc.js

<!-- Bad -->
.prettierrc.json .prettierrc
```
<!-- prettier-ignore-end -->

## End of Line

End of Line should be set to `lf`.
([`endOfLine`](https://prettier.io/docs/en/options.html#end-of-line))

> **Why?** MacOS / Linux are our primary (and recommended) development environments, thus we want to
> enforce unix-specific line endings to make it a more seamless experience on those machines.

<!-- prettier-ignore-start -->
```javascript
// Good
module.exports = {
  endOfLine: 'lf',
}

// Bad
module.exports = {
  endOfLine: 'crlf',
}
```
<!-- prettier-ignore-end -->

## Print Width

Print width should be set to `100` characters.
([`printWidth`](https://prettier.io/docs/en/options.html#print-width))

> **Why?** A 100 character limit is a standard convention at Kienle Holdings, and we want to be
> consistent across different projects, regardless of language.

<!-- prettier-ignore-start -->
```javascript
// Good
module.exports = {
  printWidth: 100,
}

// Bad
module.exports = {
  printWidth: 80,
}
```
<!-- prettier-ignore-end -->

## Prose Wrap

Prose wrap should be set to `always`.
([`proseWrap`](https://prettier.io/docs/en/options.html#prose-wrap))

> **Why?** This option is markdown specific, and will wrap lines to no more than the
> [Print Width](#print-width) whenever Prettier's format function is run, saving the developer from
> having to do it manually.

<!-- prettier-ignore-start -->
```javascript
// Good
module.exports = {
  proseWrap: 'always',
}

// Bad
module.exports = {
  proseWrap: 'never',
}

module.exports = {
  proseWrap: 'preserve',
}
```
<!-- prettier-ignore-end -->

## Single Quotes

Single quotes should be set to `true`.
([`singleQuote`](https://prettier.io/docs/en/options.html#quotes))

> **Why?** We use AirBNB's JavaScript Style guide, and this conforms to that set of standards. We
> set this globally to keep our code consistent, regardless of language or project.

<!-- prettier-ignore-start -->
```javascript
// Good
module.exports = {
  singleQuote: true,
}

// Bad
module.exports = {
  singleQuote: false,
}
```
<!-- prettier-ignore-end -->

## Trailing Comma

Trailing comma should be set to `es5`.
([`trailingComma`](https://prettier.io/docs/en/options.html#trailing-commas))

> **Why?** Having trailing commas after everything makes your code look ugly, but having `es5`
> enabled adds a reasonable amount of trailing commas that make your git diffs look a little
> cleaner.

<!-- prettier-ignore-start -->
```javascript
// Good
module.exports = {
  trailingComma: 'es5',
}

// Bad
module.exports = {
  trailingComma: 'off',
}

module.exports = {
  trailingComma: 'all',
}
```
<!-- prettier-ignore-end -->

## Resources

### Prettier

- [Project Homepage](https://prettier.io)
- [Rationale](https://prettier.io/docs/en/rationale.html)

### Tools

- [Pre-Commit Hooks for Prettier](https://prettier.io/docs/en/precommit.html)
- [Prettier for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Prettier CLI](https://prettier.io/docs/en/cli.html)

### Configurations

- [Kienle Holdings `prettier-config`](https://github.com/kienleholdings/styleguides/tree/master/packages/prettier-config)

## Amendments

This guide is subject to change. Do you see something that can be improved on? Go ahead and give it
a fork and shoot us over a PR. See an issue? Don't forget to log it!
