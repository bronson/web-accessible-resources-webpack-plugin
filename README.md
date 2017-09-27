# web-accessible-resources-webpack-plugin

This is a webpack plugin that automatically populates the `web_accessible_resources` clause in your `manifest.json`

It's handy when writing chrome extensions, especially when paired with the
[manifest loader](https://github.com/bronson/manifest-webpack-loader).

## Install

* `yarn add -D web-accessible-resources-webpack-plugin`

## Usage

```js
// webpack.config.js

const WebAccessibleResourcesPlugin = require('./src/web-accessible-resources-webpack-plugin')

module.exports = {
  ...
  plugins: [
    new WebAccessibleResourcesPlugin(/\.(png|jpg|gif)$/)
  ]
}
```

Now, any image required by your source files are will also be mentioned in
[web\_accessible\_resources](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/manifest.json/web_accessible_resources).

## Contributing

Please file an issue or pull request on [GitHub](https://github.com/bronson/web-accessible-resources-webpack-plugin/issues).

## License

MIT, be free.
