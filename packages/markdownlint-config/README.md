# MarkdownLint Config

> Kienle Holdings Markdownlint Config

## Installation

1. Install peer dependencies:
   `yarn add markdownlint-cli2 -D`
1. Install config `yarn add @kienleholdings/markdownlint-config`

## Usage

1. Add the following to your package.json
`scripts`: `"lint-markdown":"markdownlint-cli2 \"**/*.md\" \"#node_modules\""`
1. Create a file named `.markdownlint.js`
1. Add the following to the new file:

```JavaScript
module.exports = require('@kienleholdings/markdownlint-config');
```
