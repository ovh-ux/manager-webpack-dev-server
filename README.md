# Manager Webpack Dev Server

OVH manager webpack development server configuration.

## Usage

This configuration is meant to be merged with your webpack configuration using
the webpack-merge library.

```js
const merge = require('webpack-merge');
const devServer = require('manager-webpack-dev-server');
const devConfig = devServer.config(env);

module.exports = merge(yourWebpackConfig, devConfig);
```

## Env

The _env_ parameter is an object containing the following values:

```js
const env = {
  region: 'EU',     // manager region (EU, CA, US)
  local2API: false, // true to make 2API calls on local 8080 port
};
```
