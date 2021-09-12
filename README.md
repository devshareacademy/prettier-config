# prettier-config

> Shared [prettier config](https://prettier.io/docs/en/configuration.html#sharing-configurations) for my projects

## Install

```bash
yarn add -DE @scottwestover/prettier-config
```

**Note:** In order to install this package, you will need to make sure `npm` is set to download `scottwestover` scoped packages from the GitHub Package Repository. More information on this can be found here: [GitHub Install Packages](https://docs.github.com/en/packages/learn-github-packages/installing-a-package).

## Usage

`package.json`

```json
{
  "name": "some-package-name",
  "prettier": "@scottwestover/prettier-config"
}
```

If you want to extend the configuration, or not place in the `package.json`, you can place the configuration in one of the supported prettier configuration file formats. Example:

`.prettierrc.js`

```javascript
module.exports = {
  ...require("@company/prettier-config"),
  semi: false,
};
```

## Publish New Version

```bash
# Authenticate with GitHub NPM Package Registry
npm login --scope=@scottwestover --registry=https://npm.pkg.github.com

# Run publish script
yarn package-publish
```
