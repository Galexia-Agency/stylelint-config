# Stylelint Config
A base stylelint config for use across Galexia's projects

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
