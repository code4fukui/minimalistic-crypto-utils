# minimalistic-crypto-utils
非常に最小限のクリプトグラフィーを実装するのに必要なユーティリティ関数を提供するライブラリです。

## 機能
- 16進数や UTF-8 エンコーディングなどの文字列をバイト配列に変換
- バイト配列を16進数の文字列に変換
- バイト配列を任意の文字エンコーディングで表現

## 使い方
```js
import utils from "https://code4fukui.github.io/minimalistic-crypto-utils/lib/utils.js"

utils.toArray('abcd', 'hex');
utils.encode([ 1, 2, 3, 4 ], 'hex');
utils.toHex([ 1, 2, 3, 4 ]);
```

## ライセンス
このソフトウェアはMITライセンスの下でライセンスされています。

Copyright Fedor Indutny, 2017.