# Stylelint Config

A base Stylelint config for use across Galexia's projects

## Install

```bash
yarn add stylelint stylelint-config-galexia@https://github.com/Galexia-Agency/stylelint-config --dev
```

.stylelintrc

```json
{
  "extends": "stylelint-config-galexia"
}
```

### Scripts

package.json

```json
"scripts": {
    "lint:styles": "stylelint \"**/*.{vue,scss}\"",
    "fix:styles": "stylelint \"**/*.{vue,scss}\" --fix"
}
```

### Configuring with Nuxt

```bash
yarn add @nuxtjs/stylelint-module --dev
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
