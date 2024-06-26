# @devtea2026/maiores-a-est-odio <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Truly private storage, akin to the JS spec’s concept of internal slots.

Uses a WeakMap when available; a Map when not; and a regular object in even older engines. Performance and garbage collection behavior will reflect the environment’s capabilities accordingly.

## Example

```js
var SLOT = require('@devtea2026/maiores-a-est-odio');
var assert = require('assert');

var o = {};

assert.throws(function () { SLOT.assert(o, 'foo'); });

assert.equal(SLOT.has(o, 'foo'), false);
assert.equal(SLOT.get(o, 'foo'), undefined);

SLOT.set(o, 'foo', 42);

assert.equal(SLOT.has(o, 'foo'), true);
assert.equal(SLOT.get(o, 'foo'), 42);

assert.doesNotThrow(function () { SLOT.assert(o, 'foo'); });
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@devtea2026/maiores-a-est-odio
[npm-version-svg]: https://versionbadg.es/ljharb/@devtea2026/maiores-a-est-odio.svg
[deps-svg]: https://david-dm.org/ljharb/@devtea2026/maiores-a-est-odio.svg
[deps-url]: https://david-dm.org/ljharb/@devtea2026/maiores-a-est-odio
[dev-deps-svg]: https://david-dm.org/ljharb/@devtea2026/maiores-a-est-odio/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@devtea2026/maiores-a-est-odio#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@devtea2026/maiores-a-est-odio.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@devtea2026/maiores-a-est-odio.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@devtea2026/maiores-a-est-odio.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@devtea2026/maiores-a-est-odio
[codecov-image]: https://codecov.io/gh/ljharb/@devtea2026/maiores-a-est-odio/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@devtea2026/maiores-a-est-odio/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@devtea2026/maiores-a-est-odio
[actions-url]: https://github.com/devtea2026/maiores-a-est-odio/actions
