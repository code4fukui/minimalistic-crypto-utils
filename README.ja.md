# minimalistic-crypto-utils

[
![Build Status](https://secure.travis-ci.org/indutny/minimalistic-crypto-utils.svg)
](http://travis-ci.org/indutny/minimalistic-crypto-utils)
[
![NPM version](https://badge.fury.io/js/minimalistic-crypto-utils.svg)
](http://badge.fury.io/js/minimalistic-crypto-utils)

JS暗号モジュール向けの最小限のツール。

## インストール

```bash
npm install minimalistic-crypto-utils
```

## 使い方

```js
// ESM / Deno / ブラウザ
import utils from 'https://code4fukui.github.io/minimalistic-crypto-utils/lib/utils.js';

// 16進数文字列をバイト配列に変換
const bytes = utils.toArray('deadbeef', 'hex');
// => [ 222, 173, 190, 239 ]

// バイト配列を16進数文字列に変換
const hexString = utils.toHex([ 1, 10, 100, 255 ]);
// => '010a64ff'

// `encode`は`toHex`の便利なラッパー
const encoded = utils.encode([ 1, 10, 100, 255 ], 'hex');
// => '010a64ff'
```

## API

### `utils.toArray(msg, [encoding])`

メッセージ `msg` をバイト配列に変換します。

*   `msg` `<String | Array | Buffer>`: 入力メッセージ。すでに配列の場合は、そのコピーを返します。
*   `encoding` `<String>`: 省略可能なエンコーディング。
    *   `'hex'` の場合、入力文字列は16進数として扱われます。
    *   指定されない場合、文字コードに基づいて文字列がバイトに変換されます。注意: これはUTF-8エンコーディングでは**ありません**。マルチバイト文字は上位バイトと下位バイトに分割されます。

### `utils.toHex(arr)`

バイト配列 `arr` を16進数文字列に変換します。

*   `arr` `<Array>`: 変換するバイト配列。

### `utils.encode(arr, [encoding])`

配列をエンコードするための便利なラッパーです。

*   `arr` `<Array>`: 入力バイト配列。
*   `encoding` `<String>`: 省略可能なエンコーディング。
    *   `'hex'` の場合、`utils.toHex(arr)` を使用して配列を16進数文字列に変換します。
    *   それ以外の値の場合、入力配列をそのまま返します。

## ライセンス

[MIT](LICENSE) © 2017 Fedor Indutny
