# minimalistic-crypto-utils

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

[
![Build Status](https://secure.travis-ci.org/indutny/minimalistic-crypto-utils.svg)
](http://travis-ci.org/indutny/minimalistic-crypto-utils)
[
![NPM version](https://badge.fury.io/js/minimalistic-crypto-utils.svg)
](http://badge.fury.io/js/minimalistic-crypto-utils)

Minimalistic tools for JS crypto modules.

## Install

```bash
npm install minimalistic-crypto-utils
```

## Usage

```js
// ESM / Deno / Browser
import utils from 'https://code4fukui.github.io/minimalistic-crypto-utils/lib/utils.js';

// Convert a hex string to a byte array
const bytes = utils.toArray('deadbeef', 'hex');
// => [ 222, 173, 190, 239 ]

// Convert a byte array to a hex string
const hexString = utils.toHex([ 1, 10, 100, 255 ]);
// => '010a64ff'

// `encode` is a convenience wrapper for `toHex`
const encoded = utils.encode([ 1, 10, 100, 255 ], 'hex');
// => '010a64ff'
```

## API

### `utils.toArray(msg, [encoding])`

Converts a message `msg` into an array of bytes.

*   `msg` `<String | Array | Buffer>`: The input message. If already an array, a copy is returned.
*   `encoding` `<String>`: Optional encoding.
    *   If `'hex'`, the input string is treated as hexadecimal.
    *   If not provided, the string is converted to bytes based on character codes. Note: This is **not** UTF-8 encoding; multi-byte characters are split into high and low bytes.

### `utils.toHex(arr)`

Converts an array of bytes `arr` into a hexadecimal string.

*   `arr` `<Array>`: The byte array to convert.

### `utils.encode(arr, [encoding])`

A convenience wrapper for encoding an array.

*   `arr` `<Array>`: The input byte array.
*   `encoding` `<String>`: Optional encoding.
    *   If `'hex'`, it converts the array to a hex string using `utils.toHex(arr)`.
    *   If any other value, it returns the input array unmodified.

## License

[MIT](LICENSE) © 2017 Fedor Indutny