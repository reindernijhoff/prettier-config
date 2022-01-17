# MediaMonks - Prettier Configuration

The official Media.Monks prettier configuration, based on the [Frontend Coding Standards](https://github.com/mediamonks/frontend-coding-standards).

## Installation

The configuration can be installed via `npm`.

```bash
npm install --dev @mediamonks/prettier-config
```

To inform prettier of this configuration, you have to add the `prettier` property to your `package.json` file:

```json
"prettier": "@mediamonks/prettier-config"
```

Instead of manually editing your `package.json`, you can also utilize the `npm pkg` subcommand:

```bash
npm pkg set prettier=@mediamonks/prettier-config
```

## Extending

[Prettier does not ship with a built-in way of extending configurations](https://prettier.io/docs/en/configuration.html#sharing-configurations).

To extend the configuration, you will have to create a `.prettierrc.js` file (or `.prettierrc.cjs` if your package is a `"type": "module"`) and import the Media.Monks configuration using `require`:

```js
module.exports = {
  ...require("@mediamonks/prettier-config"),
  semi: false,
};
```

If you have previously added the configuration to your `package.json`, via the `prettier` property, you can now remove it.
You can also utilize the `npm pkg`:

```bash
npm pkg delete prettier
```
