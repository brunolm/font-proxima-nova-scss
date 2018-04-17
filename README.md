# font-proxima-nova

## Ionic 3

app.fonts.scss

```scss
$pn-font-path: '../assets/fonts';
@import '../../node_modules/font-proxima-nova-scss/font-proxima-nova-scss';
```

webpack-copy.config.js

```js
const defaultCopyConfig = require('@ionic/app-scripts/config/copy.config');

module.exports = {
  ...defaultCopyConfig,

  copyFonts: {
    src: [
      ...defaultCopyConfig.copyFonts.src,
      '{{ROOT}}/node_modules/font-proxima-nova/fonts/**/*',
    ],
    dest: defaultCopyConfig.copyFonts.dest,
  },
};
```

package.json

```json
  "config": {
    "ionic_copy": "./webpack-copy.config.js"
  },
```