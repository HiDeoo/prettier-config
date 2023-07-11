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

Alternatively, you can also extends the configuration through a [configuration file](https://prettier.io/docs/en/configuration.html). This is particularly useful when using some [Prettier plugins](https://prettier.io/docs/en/plugins.html):

```js
import baseConfig from '@hideoo/prettier-config'

/**
 * @type {import('prettier').Config}
 */
const prettierConfig = {
  ...baseConfig,
  plugins: ['prettier-plugin-astro'],
}

export default prettierConfig
```

### Run

Add a script in your `package.json` file to run Prettier:

```json
{
  "scripts": {
    "lint": "prettier -c --cache ."
  }
}
```

## License

Licensed under the MIT License, Copyright © HiDeoo.

See [LICENSE](https://github.com/HiDeoo/prettier-config/blob/main/LICENSE) for more information.
