# HAR Validator [![version][npm-version]][npm-url] [![License][npm-license]][license-url]

> Extremely fast HTTP Archive ([HAR](http://www.softwareishard.com/blog/har-12-spec/)) validator using JSON Schema.

[![Build Status][travis-image]][travis-url]
[![Downloads][npm-downloads]][npm-url]
[![Code Climate][codeclimate-quality]][codeclimate-url]
[![Coverage Status][codeclimate-coverage]][codeclimate-url]
[![Dependency Status][dependencyci-image]][dependencyci-url]
[![Dependencies][david-image]][david-url]

## Install

```bash
npm install --only=production --save har-validator
```

## Usage

I recommend using an optimized build matching your Node.js environment version, otherwise, the standard `require` would work just fine with any version of Node `>= v4.0` .

```js
/*
 * Node 7
 */
const har-validator = require('har-validator/lib/node7')

/*
 * Node 6
 */
const har-validator = require('har-validator/lib/node6')

/*
 * Node 4 (Default)
 * Note: additional ES2015 polyfills may be required
 */
var har-validator = require('har-validator')
```


```bash
# to use in cli
npm install --global har-validator

# to use as a module
npm install --save har-validator
```

## CLI Usage

```

  Usage: har-validator [options] <files ...>

  Options:

    -h, --help           output usage information
    -V, --version        output the version number
    -s, --schema [name]  validate schema name (log, request, response, etc ...)

```

###### Example

```shell
har-validator har.json

har-validator --schema request request.json
```

## API

**Note**: as of [`v2.0.0`](https://github.com/ahmadnassri/har-validator/releases/tag/v2.0.0) this module defaults to Promise based API. *For backward comptability with `v1.x` an [async/callback API](docs/async.md) is also provided*

- [async API](docs/async.md)
- [callback API](docs/async.md)
- [Promise API](docs/promise.md) *(default)*

----
> :copyright: [ahmadnassri.com](https://www.ahmadnassri.com/) &nbsp;&middot;&nbsp;
> License: [ISC][license-url] &nbsp;&middot;&nbsp;
> Github: [@ahmadnassri](https://github.com/ahmadnassri) &nbsp;&middot;&nbsp;
> Twitter: [@ahmadnassri](https://twitter.com/ahmadnassri)

[license-url]: http://choosealicense.com/licenses/isc/

[travis-url]: https://travis-ci.org/ahmadnassri/har-validator
[travis-image]: https://img.shields.io/travis/ahmadnassri/har-validator.svg?style=flat-square

[npm-url]: https://www.npmjs.com/package/har-validator
[npm-license]: https://img.shields.io/npm/l/har-validator.svg?style=flat-square
[npm-version]: https://img.shields.io/npm/v/har-validator.svg?style=flat-square
[npm-downloads]: https://img.shields.io/npm/dm/har-validator.svg?style=flat-square

[codeclimate-url]: https://codeclimate.com/github/ahmadnassri/har-validator
[codeclimate-quality]: https://img.shields.io/codeclimate/github/ahmadnassri/har-validator.svg?style=flat-square
[codeclimate-coverage]: https://img.shields.io/codeclimate/coverage/github/ahmadnassri/har-validator.svg?style=flat-square

[david-url]: https://david-dm.org/ahmadnassri/har-validator
[david-image]: https://img.shields.io/david/ahmadnassri/har-validator.svg?style=flat-square

[dependencyci-url]: https://dependencyci.com/github/ahmadnassri/har-validator
[dependencyci-image]: https://dependencyci.com/github/ahmadnassri/har-validator/badge?style=flat-square
