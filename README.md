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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Time

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Time utilities.

<section class="installation">

## Installation

```bash
npm install @wemnyelezxnpm/culpa-quaerat-ipsum
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var time = require( '@wemnyelezxnpm/culpa-quaerat-ipsum' );
```

#### time

Namespace containing time utilities.

```javascript
var ns = time;
// returns {...}
```

### Calendar Utilities

<!-- <toc keywords="+calendar"> -->

<div class="namespace-toc">

-   <span class="signature">[`dayOfQuarter( [month[, day, year]] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/day-of-quarter]</span><span class="delimiter">: </span><span class="description">determine the day of the quarter.</span>
-   <span class="signature">[`dayOfYear( [month[, day, year]] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/day-of-year]</span><span class="delimiter">: </span><span class="description">determine the day of the year.</span>
-   <span class="signature">[`daysInMonth( [month[, year]] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/days-in-month]</span><span class="delimiter">: </span><span class="description">determine the number of days in a month.</span>
-   <span class="signature">[`daysInYear( [value] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/days-in-year]</span><span class="delimiter">: </span><span class="description">determine the number of days in a year according to the Gregorian calendar.</span>
-   <span class="signature">[`hoursInMonth( [month[, year]] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/hours-in-month]</span><span class="delimiter">: </span><span class="description">determine the number of hours in a month.</span>
-   <span class="signature">[`hoursInYear( [value] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/hours-in-year]</span><span class="delimiter">: </span><span class="description">determine the number of hours in a year according to the Gregorian calendar.</span>
-   <span class="signature">[`isoWeeksInYear( [value] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/iso-weeks-in-year]</span><span class="delimiter">: </span><span class="description">determine the number of ISO weeks in a year according to the Gregorian calendar.</span>
-   <span class="signature">[`minutesInMonth( [month[, year]] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/minutes-in-month]</span><span class="delimiter">: </span><span class="description">determine the number of minutes in a month.</span>
-   <span class="signature">[`minutesInYear( [value] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/minutes-in-year]</span><span class="delimiter">: </span><span class="description">determine the number of minutes in a year according to the Gregorian calendar.</span>
-   <span class="signature">[`quarterOfYear( [month] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/quarter-of-year]</span><span class="delimiter">: </span><span class="description">determine the quarter of the year.</span>
-   <span class="signature">[`secondsInMonth( [month[, year]] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/seconds-in-month]</span><span class="delimiter">: </span><span class="description">determine the number of seconds in a month.</span>
-   <span class="signature">[`secondsInYear( [value] )`][@wemnyelezxnpm/culpa-quaerat-ipsum/seconds-in-year]</span><span class="delimiter">: </span><span class="description">determine the number of seconds in a year according to the Gregorian calendar.</span>

</div>

<!-- </toc> -->

```javascript
var num = time.daysInYear( 2000 );
// returns 366

num = time.hoursInMonth( 2, 2017 );
// returns 672
```

### Timer Utilities

<!-- <toc keywords="+timer"> -->

<div class="namespace-toc">

-   <span class="signature">[`tic()`][@wemnyelezxnpm/culpa-quaerat-ipsum/tic]</span><span class="delimiter">: </span><span class="description">return a high-resolution time.</span>
-   <span class="signature">[`toc( time )`][@wemnyelezxnpm/culpa-quaerat-ipsum/toc]</span><span class="delimiter">: </span><span class="description">return a high-resolution time difference.</span>

</div>

<!-- </toc> -->

```javascript
var time = require( '@wemnyelezxnpm/culpa-quaerat-ipsum' );

var start = time.tic();

setTimeout( onTimeout, 2000 );

function onTimeout() {
    var elapsed = time.toc( start );
    console.log( 'Elapsed: %d seconds and %d nanoseconds', elapsed[0], elapsed[1] );
}
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var time = require( '@wemnyelezxnpm/culpa-quaerat-ipsum' );

console.log( objectKeys( time ) );
```

</section>

<!-- /.examples -->

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@wemnyelezxnpm/culpa-quaerat-ipsum.svg
[npm-url]: https://npmjs.org/package/@wemnyelezxnpm/culpa-quaerat-ipsum

[test-image]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/wemnyelezxnpm/culpa-quaerat-ipsum/main.svg
[coverage-url]: https://codecov.io/github/wemnyelezxnpm/culpa-quaerat-ipsum?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/wemnyelezxnpm/culpa-quaerat-ipsum.svg
[dependencies-url]: https://david-dm.org/wemnyelezxnpm/culpa-quaerat-ipsum/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/deno
[deno-readme]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/blob/deno/README.md
[umd-url]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/umd
[umd-readme]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/blob/umd/README.md
[esm-url]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/esm
[esm-readme]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/blob/esm/README.md
[branches-url]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/wemnyelezxnpm/culpa-quaerat-ipsum/main/LICENSE

<!-- <toc-links> -->

[@wemnyelezxnpm/culpa-quaerat-ipsum/tic]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/tic

[@wemnyelezxnpm/culpa-quaerat-ipsum/toc]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/toc

[@wemnyelezxnpm/culpa-quaerat-ipsum/day-of-quarter]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/day-of-quarter

[@wemnyelezxnpm/culpa-quaerat-ipsum/day-of-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/day-of-year

[@wemnyelezxnpm/culpa-quaerat-ipsum/days-in-month]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/days-in-month

[@wemnyelezxnpm/culpa-quaerat-ipsum/days-in-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/days-in-year

[@wemnyelezxnpm/culpa-quaerat-ipsum/hours-in-month]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/hours-in-month

[@wemnyelezxnpm/culpa-quaerat-ipsum/hours-in-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/hours-in-year

[@wemnyelezxnpm/culpa-quaerat-ipsum/iso-weeks-in-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/iso-weeks-in-year

[@wemnyelezxnpm/culpa-quaerat-ipsum/minutes-in-month]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/minutes-in-month

[@wemnyelezxnpm/culpa-quaerat-ipsum/minutes-in-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/minutes-in-year

[@wemnyelezxnpm/culpa-quaerat-ipsum/quarter-of-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/quarter-of-year

[@wemnyelezxnpm/culpa-quaerat-ipsum/seconds-in-month]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/seconds-in-month

[@wemnyelezxnpm/culpa-quaerat-ipsum/seconds-in-year]: https://github.com/wemnyelezxnpm/culpa-quaerat-ipsum/tree/main/seconds-in-year

<!-- </toc-links> -->

</section>

<!-- /.links -->
