# ES6 native module fork
This fork provides a browser friendly export of the module at /es/index.js (ES6 JavaScript native module).
That export includes all dependencies in one file so as to reduce http calls.
The /es/index-nodeps.js file is similar but does not include dependencies. This one is for build optimization.
The purpose of this and similar forks is to be able to load JS native modules and their dependencies from npm.

string-hash
===========

A fast string hashing function for Node.JS. The particular algorithm is quite
similar to `djb2`, by Dan Bernstein and available
[here](http://www.cse.yorku.ca/~oz/hash.html). Differences include iterating
over the string *backwards* (as that is faster in JavaScript) and using the XOR
operator instead of the addition operator (as described at that page and
because it obviates the need for modular arithmetic in JavaScript).

The hashing function returns a number between 0 and 4294967295 (inclusive).

Thanks to [cscott](https://github.com/cscott) for reminding us how integers
work in JavaScript.

Example
-------

`npm install string-hash` or `yarn add string-hash`, then:

```
import stringHash from "string-hash";
const myString = "foo";
const myPositiveInteger = stringHash(myString);
```

Note that the return value is always an unsigned, 32-bit integer.

License
-------

To the extend possible by law, The Dark Sky Company, LLC has [waived all
copyright and related or neighboring rights][cc0] to this library.

[cc0]: http://creativecommons.org/publicdomain/zero/1.0/
