# Prettier Config

[Prettier](https://prettier.io/) config file as an npm package.

## Installation

Using `npm`:

```
npm install --save-dev @kdbcinco/prettier-config
```

Using `yarn`:

```
yarn add --dev @kdbcinco/prettier-config
```

**NOTE:** The instructions above assume that Prettier is already installed.

We can then use this module:

Using `prettier.config.js`:

```javascript
// We can export the name of this module
module.exports = '@kdbcinco/prettier-config';

// Or import
module.exports = {
  ...require('@kbcinco/prettier-config'),
  // we can then extend the config
  printWidth: 90001,
};
```

Or, using `prettier` field on `package.json`:

```json
{
  "name": "my-very-awesome-app",
  "version" "3.10.11",
  "prettier": "@kdbcinco/prettier-config"
}
```

## Options

| Option          | Value  |
| --------------- | ------ |
| `singleQuote`   | `true` |
| `trailingComma` | `all`  |

## Additional Information

The module consists of an entry point `index.js` which imports `.prettierrc.json`. The JSON configuration file makes of the Prettier [schema](http://json.schemastore.org/prettierrc) to take advantage of VSCode's autocompletion.
