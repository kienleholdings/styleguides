# ESLint Config Base

> Kienle Holdings Base (Non-React) ESLint Config

## Installation

1. Install peer dependencies:
   `yarn add typescript eslint prettier @kienleholdings/prettier-config -D`
1. Install config `yarn add @kienleholdings/eslint-config-base`

## Usage

1. Create a file named `.eslintrc.js`
1. Add the following:

```JavaScript
module.exports = {
  extends: [
    '@kienleholdings/base',
  ],
};
```
