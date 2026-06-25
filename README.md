![Seneca](http://senecajs.org/files/assets/seneca-logo.png)
> A [Seneca.js][] plugin

# @seneca/web-adapter-koa1


[![npm version](https://img.shields.io/npm/v/@seneca/web-adapter-koa1.svg)](https://npmjs.com/package/@seneca/web-adapter-koa1)
[![build](https://github.com/senecajs/seneca-web-adapter-koa1/actions/workflows/build.yml/badge.svg)](https://github.com/senecajs/seneca-web-adapter-koa1/actions/workflows/build.yml)
[![Known Vulnerabilities](https://snyk.io/test/github/senecajs/seneca-web-adapter-koa1/badge.svg)](https://snyk.io/test/github/senecajs/seneca-web-adapter-koa1)

| ![Voxgig](https://www.voxgig.com/res/img/vgt01r.png) | This open source module is sponsored and supported by [Voxgig](https://www.voxgig.com). |
|---|---|

## Install

```sh
npm install seneca-web-adapter-koa1
```

## Quick Example

```js
var SenecaWeb = require('seneca-web')
var Koa = require('koa')
var app = new Koa()
require('seneca')()
  .use(SenecaWeb, { context: app, adapter: require('seneca-web-adapter-koa1') })
```

## More Examples

See [test/](test/) for usage examples.

## Motivation

Koa v1 adapter for [seneca-web](https://github.com/senecajs/seneca-web). Maps HTTP routes to Seneca actions.

## Support

If you're using this module and need help, you can:

- Post a [github issue][]
- Tweet to [@senecajs][]

## API

Configured via [seneca-web](https://github.com/senecajs/seneca-web) options.

## Contributing

The [Senecajs org][] encourages open participation. If you feel you can help in any way, be it with documentation, examples, extra testing, or new features please get in touch.

### Running tests

```sh
npm run test
```

## Background

Part of the [seneca-web](https://github.com/senecajs/seneca-web) adapter family. For Koa v2 see [seneca-web-adapter-koa2](https://github.com/senecajs/seneca-web-adapter-koa2).


