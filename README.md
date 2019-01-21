# Decorator Cache Getter

[![NPM version][npm-image]][npm-url]
[![NPM downloads][downloads-image]][downloads-url]
[![Build status][travis-image]][travis-url]
[![Test coverage][coveralls-image]][coveralls-url]

> Simple decorator for caching getters on first access.

## Installation

```sh
npm install decorator-cache-getter --save
```

## Usage

```js
import { cache } from "decorator-cache-getter";

class User {
  @cache
  get friends() {
    return sql("SELECT * FROM users WHERE ...")
  }
}

const user = new User()
const friends = await user.friends;
```

## License

MIT

[npm-image]: https://img.shields.io/npm/v/decorator-cache-getter.svg?style=flat
[npm-url]: https://npmjs.org/package/decorator-cache-getter
[downloads-image]: https://img.shields.io/npm/dm/decorator-cache-getter.svg?style=flat
[downloads-url]: https://npmjs.org/package/decorator-cache-getter
[travis-image]: https://img.shields.io/travis/blakeembrey/decorator-cache-getter.svg?style=flat
[travis-url]: https://travis-ci.org/blakeembrey/decorator-cache-getter
[coveralls-image]: https://img.shields.io/coveralls/blakeembrey/decorator-cache-getter.svg?style=flat
[coveralls-url]: https://coveralls.io/r/blakeembrey/decorator-cache-getter?branch=master
