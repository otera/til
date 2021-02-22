# HTMLメモ

## Canvas

図形を描くためのHTML5から利用可能な技術仕様で、HTMLのcanvas要素とJavaScriptを組み合わせて図形を描画します。  
Canvas自体は「ただ何かを描くための領域」であり、CanvasRenderingContext2DはCanvas独自のAPIで2Dの描画をすることができる。

## WebGL

WebGLはOpenGLのグラフィックAPIをCanvas上で使える様にした物で、OSに依存することなくウェブブラウザ上での3DCG表示を可能にしたもの。  
CPUではなくGPUにて処理を行うため、グラフィックスを高速に描画します。  
WebGL=3Dではなく、2Dの描画処理も可能です。

### PixiJS

PixiJSはWebGLでの2D表現を作りやすくするレンダリングJSライブラリ。  
PixiJSのv5でWebGLの利用が必須になっている為、例えばChromeのハードウェアアクセラレーションを無効にしていると描画ができずにエラーが発生する。  
v5より前のバージョンか、pixi-legacy.jsを使うとCanvas2Dへのフォールバックが有効になる。

## WebGPU

WebGLの次世代のウェブブラウザ用3DグラフィックスAPIで、 WebGLやWebGL2の後継とされている。  
WebGPUは、より低レベルなGPUアクセスを目的としたAPIの為、WebGLに比べパフォーマンスの向上が期待されている。

[次世代仕様のWebGPUとは？　次期macOSでのOpenGL非推奨化はWebGLに影響をもたらすのか \- ICS MEDIA](https://ics.media/entry/18412/)
