![Seneca](http://senecajs.org/files/assets/seneca-logo.png)
> A [Seneca.js][] plugin

# @seneca/web-adapter-koa1

[![npm version](https://img.shields.io/npm/v/seneca-web-adapter-koa1.svg)](https://npmjs.com/package/seneca-web-adapter-koa1)
[![build](https://github.com/senecajs/seneca-web-adapter-koa1/actions/workflows/build.yml/badge.svg)](https://github.com/senecajs/seneca-web-adapter-koa1/actions/workflows/build.yml)
[![Known Vulnerabilities](https://snyk.io/test/github/senecajs/seneca-web-adapter-koa1/badge.svg)](https://snyk.io/test/github/senecajs/seneca-web-adapter-koa1)
[![Coverage Status](https://coveralls.io/repos/github/senecajs/seneca-web-adapter-koa1/badge.svg?branch=master)](https://coveralls.io/github/senecajs/seneca-web-adapter-koa1?branch=master)

| ![Voxgig](https://www.voxgig.com/res/img/vgt01r.png) | This open source module is sponsored and supported by [Voxgig](https://www.voxgig.com). |
|---|---|

## Install

Peer dependencies have been specified for `koa`, `koa-router` and `seneca-web`. They need to be present for this to work at all.

```sh
npm install --save koa
npm install --save koa-router
npm install --save seneca
npm install --save seneca-web
npm install --save seneca-web-adapter-koa1
```js

## Quick Example

```js
const Seneca = require('seneca')
const SenecaWeb = require('seneca-web')
const Koa = require('koa')
const Router = require('koa-router')
const app = Koa()
const seneca = Seneca()
seneca.use(SenecaWeb, {
  context: Router(),
  adapter: require('seneca-web-adapter-koa1')
})
seneca.ready(() => {
  app.use(seneca.export('web/context')().routes())
})
```js

## More Examples

See [test/](test/) for usage examples.

## Motivation

Koa v1 adapter for [seneca-web](https://github.com/senecajs/seneca-web). Maps HTTP routes to Seneca actions.

## Support

If you're using this module and need help, you can:

- Post a [github issue](https://github.com/senecajs/seneca-web-adapter-koa1/issues)
- Tweet to [@senecajs](http://twitter.com/senecajs)
- Ask on the [Gitter](https://gitter.im/senecajs/seneca)

## API

Please refer to the [seneca-web](https://github.com/senecajs/seneca-web) documentation on how to load routes.

> **Note:** Most of the seneca-web documents refer to passing the application as the `context` parameter. Doing this with Koa will result in unexpected errors — Koa Router must be used instead.

## Contributing

The [Senecajs org][] encourages open participation. If you feel you can help in any way, be it with documentation, examples, extra testing, or new features please get in touch.

### Running tests

```sh
npm run test
```js

## Background

Part of the [seneca-web](https://github.com/senecajs/seneca-web) adapter family. For Koa v2 see [seneca-web-adapter-koa2](https://github.com/senecajs/seneca-web-adapter-koa2).

[Senecajs org]: https://github.com/senecajs/
[Seneca.js]: https://www.npmjs.com/package/seneca
