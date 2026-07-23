# vendor/

このディレクトリには、LP を外部 CDN に依存させず自己完結させるために同梱した
サードパーティ資産を置いています。ネット接続なしでも `index.html` を直接開けば動作します。

## three.min.js
- ライブラリ: three.js
- バージョン: r128 (0.128.0)
- ビルド: UMD グローバルビルド (`build/three.min.js`)。`file://` で直接開いても
  ES module の CORS 制約に当たらないため、あえてグローバルビルドを採用。
- ライセンス: MIT (`LICENSE-three.txt` を参照)
- 取得元: npm レジストリ (`npm pack three@0.128.0`) から `build/three.min.js` を抽出。

ヒーローの 3D ビジュアルはこのライブラリを使い、ジオメトリはすべてコード内で
生成しています(外部の .glb 等のモデルファイルは同梱していません)。

## LICENSE-three.txt
three.js の MIT ライセンス全文。
