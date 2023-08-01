<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Kurtosis

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Laplace][laplace-distribution] distribution [excess kurtosis][kurtosis].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [excess kurtosis][kurtosis] for a [Laplace][laplace-distribution] random variable with location parameter `mu` and scale parameter `b > 0` is

<!-- <equation class="equation" label="eq:laplace_kurtosis" align="center" raw="\operatorname{Kurt}\left( X \right) = 3" alt="Excess kurtosis for a Laplace distribution."> -->

```math
\mathop{\mathrm{Kurt}}\left( X \right) = 3
```

<!-- <div class="equation" align="center" data-raw-text="\operatorname{Kurt}\left( X \right) = 3" data-equation="eq:laplace_kurtosis">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/laplace/kurtosis/docs/img/equation_laplace_kurtosis.svg" alt="Excess kurtosis for a Laplace distribution.">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/stats-base-dists-laplace-kurtosis
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

</section>

<section class="usage">

## Usage

```javascript
var kurtosis = require( '@stdlib/stats-base-dists-laplace-kurtosis' );
```

#### kurtosis( mu, b )

Returns the [excess kurtosis][kurtosis] for a [Laplace][laplace-distribution] distribution with location parameter `mu` and scale parameter `b`.

```javascript
var y = kurtosis( 2.0, 1.0 );
// returns 3.0

y = kurtosis( 0.0, 1.0 );
// returns 3.0

y = kurtosis( -1.0, 4.0 );
// returns 3.0
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var y = kurtosis( NaN, 1.0 );
// returns NaN

y = kurtosis( 0.0, NaN );
// returns NaN
```

If provided `b <= 0`, the function returns `NaN`.

```javascript
var y = kurtosis( 0.0, 0.0 );
// returns NaN

y = kurtosis( 0.0, -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var kurtosis = require( '@stdlib/stats-base-dists-laplace-kurtosis' );

var mu;
var b;
var y;
var i;

for ( i = 0; i < 10; i++ ) {
    mu = ( randu()*10.0 ) - 5.0;
    b = randu() * 20.0;
    y = kurtosis( mu, b );
    console.log( 'µ: %d, b: %d, Kurt(X;µ,b): %d', mu.toFixed( 4 ), b.toFixed( 4 ), y.toFixed( 4 ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-laplace-kurtosis.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-laplace-kurtosis

[test-image]: https://github.com/stdlib-js/stats-base-dists-laplace-kurtosis/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/stats-base-dists-laplace-kurtosis/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-laplace-kurtosis/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-laplace-kurtosis?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-laplace-kurtosis.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-laplace-kurtosis/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-laplace-kurtosis/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-laplace-kurtosis/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-laplace-kurtosis/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-laplace-kurtosis/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-laplace-kurtosis/main/LICENSE

[laplace-distribution]: https://en.wikipedia.org/wiki/Laplace_distribution

[kurtosis]: https://en.wikipedia.org/wiki/Kurtosis

</section>

<!-- /.links -->
