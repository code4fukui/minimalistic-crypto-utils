# minimalistic-crypto-utils
[![Build Status](https://secure.travis-ci.org/indutny/minimalistic-crypto-utils.svg)](http://travis-ci.org/indutny/minimalistic-crypto-utils)
[![NPM version](https://badge.fury.io/js/minimalistic-crypto-utils.svg)](http://badge.fury.io/js/minimalistic-crypto-utils)

Very minimal utils that are required in order to write reasonable JS-only
crypto module.

## Usage

```js
import utils from "https://code4fukui.github.io/minimalistic-crypto-utils/lib/utils.js"

utils.toArray('abcd', 'hex');
utils.encode([ 1, 2, 3, 4 ], 'hex');
utils.toHex([ 1, 2, 3, 4 ]);
```

#### LICENSE

This software is licensed under the MIT License.

Copyright Fedor Indutny, 2017.

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to permit
persons to whom the Software is furnished to do so, subject to the
following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN
NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE
USE OR OTHER DEALINGS IN THE SOFTWARE.

[0]: http://tools.ietf.org/html/rfc6979
[1]: https://github.com/indutny/bn.js
[2]: https://github.com/indutny/hash.js
[3]: https://github.com/bitchan/eccrypto
[4]: https://github.com/wanderer/secp256k1-node
