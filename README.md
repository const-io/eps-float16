EPSILON
===
[![NPM version][npm-image]][npm-url] [![Build Status][build-image]][build-url] [![Coverage Status][coverage-image]][coverage-url] [![Dependencies][dependencies-image]][dependencies-url]

> Difference between one and the smallest value greater than one that can be represented as a [half-precision floating-point number][ieee754].

[Epsilon][machine-epsilon] is defined as

<div class="equation" align="center" data-raw-text="\epsilon = b^{-(p-1)}" data-equation="eq:epsilon_float16">
	<img src="https://cdn.rawgit.com/const-io/eps-float16/2e220c45c59485fea715d7e7081c30e241703bb0/docs/img/epsilon.svg" alt="Epsilon for a floating-point number.">
	<br>
	<br>
</div>

where `b` is the radix (base) and `p` is the precision (number of radix bits in the significand). For [half-precision floating-point numbers][ieee754], `b` is `2` and `p` is `11`.


## Installation

``` bash
$ npm install const-eps-float16
```


## Usage

``` javascript
var FLOAT16_EPSILON = require( 'const-eps-float16' );
```

#### FLOAT16_EPSILON

Difference between one and the smallest value greater than one that can be represented as a [half-precision floating-point number][ieee754].

``` javascript
FLOAT16_EPSILON === 0.0009765625;
```


## Examples

``` javascript
var FLOAT16_EPSILON = require( 'const-eps-float16' );

console.log( FLOAT16_EPSILON );
// returns 0.0009765625
```

To run the example code from the top-level application directory,

``` bash
$ node ./examples/index.js
```


---
## Tests

### Unit

This repository uses [tape][tape] for unit tests. To run the tests, execute the following command in the top-level application directory:

``` bash
$ make test
```

All new feature development should have corresponding unit tests to validate correct functionality.


### Test Coverage

This repository uses [Istanbul][istanbul] as its code coverage tool. To generate a test coverage report, execute the following command in the top-level application directory:

``` bash
$ make test-cov
```

Istanbul creates a `./reports/coverage` directory. To access an HTML version of the report,

``` bash
$ make view-cov
```


### Browser Support

This repository uses [Testling][testling] for browser testing. To run the tests in a (headless) local web browser, execute the following command in the top-level application directory:

``` bash
$ make test-browsers
```

To view the tests in a local web browser,

``` bash
$ make view-browser-tests
```

<!-- [![browser support][browsers-image]][browsers-url] -->


---
## License

[MIT license](http://opensource.org/licenses/MIT).


## Copyright

Copyright &copy; 2016. The [Compute.io][compute-io] Authors.


[npm-image]: http://img.shields.io/npm/v/const-eps-float16.svg
[npm-url]: https://npmjs.org/package/const-eps-float16

[build-image]: http://img.shields.io/travis/const-io/eps-float16/master.svg
[build-url]: https://travis-ci.org/const-io/eps-float16

[coverage-image]: https://img.shields.io/codecov/c/github/const-io/eps-float16/master.svg
[coverage-url]: https://codecov.io/github/const-io/eps-float16?branch=master

[dependencies-image]: http://img.shields.io/david/const-io/eps-float16.svg
[dependencies-url]: https://david-dm.org/const-io/eps-float16

[dev-dependencies-image]: http://img.shields.io/david/dev/const-io/eps-float16.svg
[dev-dependencies-url]: https://david-dm.org/dev/const-io/eps-float16

[github-issues-image]: http://img.shields.io/github/issues/const-io/eps-float16.svg
[github-issues-url]: https://github.com/const-io/eps-float16/issues

[tape]: https://github.com/substack/tape
[istanbul]: https://github.com/gotwarlost/istanbul
[testling]: https://ci.testling.com

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985
[compute-io]: https://github.com/compute-io
[machine-epsilon]: https://en.wikipedia.org/wiki/Machine_epsilon
