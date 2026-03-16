# minimalistic-crypto-utils

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

Very minimal utils that are required in order to write reasonable JS-only crypto module.

[![Build Status](https://secure.travis-ci.org/indutny/minimalistic-crypto-utils.svg)](http://travis-ci.org/indutny/minimalistic-crypto-utils)
[![NPM version](https://badge.fury.io/js/minimalistic-crypto-utils.svg)](http://badge.fury.io/js/minimalistic-crypto-utils)

## Usage

```js
import utils from "https://code4fukui.github.io/minimalistic-crypto-utils/lib/utils.js"

utils.toArray('abcd', 'hex');
utils.encode([ 1, 2, 3, 4 ], 'hex');
utils.toHex([ 1, 2, 3, 4 ]);
```

## License

MIT License — see [LICENSE](LICENSE).