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

# FLOAT32_SQRT_EPS

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Square root][@stdlib/math/base/special/sqrt] of [single-precision floating-point epsilon][@stdlib/constants/float32/eps].



<section class="usage">

## Usage

To use in Observable,

```javascript
FLOAT32_SQRT_EPS = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-sqrt-eps@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var FLOAT32_SQRT_EPS = require( 'path/to/vendor/umd/constants-float32-sqrt-eps/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-sqrt-eps@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.FLOAT32_SQRT_EPS;
})();
</script>
```

#### FLOAT32_SQRT_EPS

[Square root][@stdlib/math/base/special/sqrt] of [single-precision floating-point epsilon][@stdlib/constants/float32/eps].

```javascript
var bool = ( FLOAT32_SQRT_EPS === 0.0003452669770922512 );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-abs@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-max@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-float64-base-to-float32@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-sqrt-eps@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var bool;
var a;
var b;
var i;

function isApprox( a, b ) {
    var delta;
    var tol;

    delta = float64ToFloat32( abs( a - b ) );
    tol = float64ToFloat32( FLOAT32_SQRT_EPS * max( abs( a ), abs( b ) ) );

    return ( delta <= tol );
}

for ( i = 0; i < 100; i++ ) {
    a = float64ToFloat32( randu()*10.0 );
    b = float64ToFloat32( a + (randu()*2.0e-2) - 1.0e-2 );
    bool = isApprox( a, b );
    console.log( '%d %s approximately equal to %d', a, ( bool ) ? 'is' : 'is not', b );
}

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/constants-float32/eps`][@stdlib/constants/float32/eps]</span><span class="delimiter">: </span><span class="description">difference between one and the smallest value greater than one that can be represented as a single-precision floating-point number.</span>
-   <span class="package-name">[`@stdlib/constants-float64/sqrt-eps`][@stdlib/constants/float64/sqrt-eps]</span><span class="delimiter">: </span><span class="description">square root of double-precision floating-point epsilon.</span>

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float32-sqrt-eps.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float32-sqrt-eps

[test-image]: https://github.com/stdlib-js/constants-float32-sqrt-eps/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/constants-float32-sqrt-eps/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float32-sqrt-eps/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float32-sqrt-eps?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float32-sqrt-eps.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float32-sqrt-eps/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/constants-float32-sqrt-eps/tree/deno
[umd-url]: https://github.com/stdlib-js/constants-float32-sqrt-eps/tree/umd
[esm-url]: https://github.com/stdlib-js/constants-float32-sqrt-eps/tree/esm
[branches-url]: https://github.com/stdlib-js/constants-float32-sqrt-eps/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float32-sqrt-eps/main/LICENSE

[@stdlib/math/base/special/sqrt]: https://github.com/stdlib-js/math-base-special-sqrt/tree/umd

<!-- <related-links> -->

[@stdlib/constants/float32/eps]: https://github.com/stdlib-js/constants-float32-eps/tree/umd

[@stdlib/constants/float64/sqrt-eps]: https://github.com/stdlib-js/constants-float64-sqrt-eps/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
