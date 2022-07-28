<div align="center">
  <h1>@hideoo/prettier-config 📐</h1>
  <p>HiDeoo's Prettier configuration</p>
</div>

<div align="center">
  <a href="https://github.com/HiDeoo/prettier-config/blob/main/LICENSE">
    <img alt="License" src="https://badgen.net/github/license/hideoo/prettier-config" />
  </a>
  <br /><br />
</div>

## Usage

### Install

```shell
$ pnpm add -D prettier @hideoo/prettier-config
```

### Configure

Reference the configuration in your `package.json` file:

```json
{
  "prettier": "@hideoo/prettier-config"
}
```

Alternatively, you can also extends the configuration through a `.prettierrc.cjs` configuration file. This is particularly useful when using some [Prettier plugins](https://prettier.io/docs/en/plugins.html) with a package manager like [pnpm](https://pnpm.io) or [Yarn PnP](https://yarnpkg.com/features/pnp) which [breaks plugin autoloading](https://github.com/prettier/prettier/issues/8474):

```js
const baseConfig = require('@hideoo/prettier-config')

/**
 * @type {import('prettier').Config}
 */
const prettierConfig = {
  ...baseConfig,
  plugins: [require.resolve('prettier-plugin-tailwindcss')],
}

module.exports = prettierConfig
```

## License

Licensed under the MIT License, Copyright © HiDeoo.

See [LICENSE](https://github.com/HiDeoo/prettier-config/blob/main/LICENSE) for more information.
