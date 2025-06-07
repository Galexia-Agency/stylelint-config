# Stylelint Config

A base Stylelint config for use across Galexia's projects

## Install

```bash
pnpm add -D stylelint @galexia-agency/stylelint-config-galexia
```

### Add the GitHub registry

Create or update a `.npmrc` file and include:

```ini
@galexia-agency:registry=https://npm.pkg.github.com
//npm.pkg.github.com/:_authToken=<GITHUB_TOKEN>
```

Replace `<GITHUB_TOKEN>` with a [personal access token](https://github.com/settings/tokens) that has `read:packages` permissions.

### Scripts

package.json

```json
"scripts": {
    "lint:styles": "stylelint \"**/*.{vue,scss}\"",
    "fix:styles": "stylelint \"**/*.{vue,scss}\" --fix"
}
```

### Configuration

.stylelintrc

```json
{
  "extends": "stylelint-config-galexia"
}
```

### Configuring with Nuxt

```bash
pnpm add -D @nuxtjs/stylelint-module
```

nuxt.config.js

```js
...
modules: [
    '@nuxtjs/stylelint-module',
]
...
```

### Configuring with VSCode

1. Install [stylelint.vscode-stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint)
2. Add `scss` and `vue` to `Snippet` and `Validate` plugin settings.
3. Add the following to `.vscode/settings.json`

  ```json
  {
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  }
  ```
