# Prettier Config

> Kienle Holdings Prettier configuration

## Installation

1. Install peer dependencies: `yarn add prettier@2.2.1 -D`
1. Install config `yarn add @kienleholdings/prettier-config`

## Usage

1. Add the following to your project's `package.json`:
   `"prettier": "@kienleholdings/prettier-config",`
1. Done (yup, that's really all there is)

## Advanced Usage

1. Create a `.prettierrc.js`.
1. Add the code: `module.exports = { ...require('@kienleholdings/prettier-config') };`
1. Done. Feel free to make any further modifications in that object.
