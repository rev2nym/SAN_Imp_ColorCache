# SAN_Imp_ColorCache
このスクリプトはRPGツクールMV向けパフォーマンス改善プラグインです。

## 概要
色データの取得結果をキャッシュ化することでゲームの処理速度の改善を図ります。
テキストカラーやゲージカラーを毎フレーム取得して
ウィンドウやスプライトを毎フレーム再描画するようなゲームの
処理速度の改善により効果を発揮します。

## 詳細
「Bitmap.getPixel()」メソッドと「Bitmap.getAlphaPixel()」メソッドの結果を
キャッシュ化することで「CanvasRenderingContext2D.getImageData()」メソッドの
呼び出し回数を削減し Major GC の回数を削減する効果が期待できます。
これらの処理は主に「Window_Base.textColor()」メソッドと
「Window_Base.pendingColor()」メソッドで使用されており
ウィンドウに関係する大抵の色データ取得メソッドで使用されています。

## 使い方
次のリンク先のファイルを保存してプラグインとして適用してください。   
https://raw.githubusercontent.com/rev2nym/SAN_Imp_ColorCache/master/js/plugins/SAN_Imp_ColorCache.js

## 利用規約
MITライセンスのもと、商用利用、改変、再配布が可能です。
ただし冒頭のコメントは削除や改変をしないでください。
これを利用したことによるいかなる損害にも作者は責任を負いません。
サポートは期待しないでください＞＜。
