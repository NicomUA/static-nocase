# static-nocase

[![NPM Version][npm-image]][npm-url]
[![NPM Downloads][downloads-image]][downloads-url]


## Install

```sh
$ npm install statc-nocase
```

## API

```js
var static = require('static-nocase')
```

### static(root, options)

Create a new middleware function to serve files from within a given root
directory. The file to serve will be determined by combining `req.url`
with the provided root directory. When a file is not found, instead of
sending a 404 response, this module will instead call `next()` to move on
to the next middleware, allowing for stacking and fall-backs.

## Examples

### Serving using express

```js
var app = require('express')(),
    static = require('./static-nocase')

app.use(static(__dirname + '/static'))

// Listen
server.listen(3000)
```

## License

[MIT](LICENSE)

[npm-image]: https://img.shields.io/npm/v/static-nocase.svg?style=flat
[npm-url]: https://npmjs.org/package/static-nocase
[downloads-image]: https://img.shields.io/npm/dm/static-nocase.svg?style=flat
[downloads-url]: https://npmjs.org/package/static-nocase
