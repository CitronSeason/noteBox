
[https://self-development.info/onnx-runtime（gpu版）のインストール/](https://self-development.info/onnx-runtime%EF%BC%88gpu%E7%89%88%EF%BC%89%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB/)

[https://self-development.info/tensorflow-1系gpu版のためにcuda-10-0をインストール/](https://self-development.info/tensorflow-1%e7%b3%bbgpu%e7%89%88%e3%81%ae%e3%81%9f%e3%82%81%e3%81%abcuda-10-0%e3%82%92%e3%82%a4%e3%83%b3%e3%82%b9%e3%83%88%e3%83%bc%e3%83%ab/)

[https://onnxruntime.ai/](https://onnxruntime.ai/)

[https://github.com/microsoft/onnxruntime/releases](https://github.com/microsoft/onnxruntime/releases)

Table of Contents

1. 事前知識
    1. RobustVideoMatting(RVM)とは
    1. onnxruntimeとは
    1. pyenvとvenvを使用する理由
2. python(pyenv + venv)導入
    1. pyenvを入れる
    2. venvを入れる
3. RVM環境構築
    1. CUDA + cudnnを導入する
    2. RVMに必要なライブラリを導入する
4. TouchDesignerにRVMの環境を適用させる
5. TD上でプログラムを書く
    1. TDからpythonに画像をおくる
    2. python上でRVMに適したデータ形式に整形する
    3. 結果をTDに送る
    4. Composite

## 事前知識
### RobustVideoMatting(RVM)とは
http://cedro3.com/ai/rvm/
cedroさんの記事がわかりやすいです。

いわゆる人物切り抜きで、Zoomのバーチャル背景などに応用されています。
RVMはそのうちの一つで精度が高く、かつ高速に動作するということで注目されています。
Cedroさんのツイート

https://twitter.com/jun40vn/status/1462707427472818176?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1462707427472818176%7Ctwgr%5E96ad48c6c20632cf4d6094ef20ccdbf31e79242a%7Ctwcon%5Es1_c10&ref_url=http%3A%2F%2Fcedro3.com%2Fai%2Frvm%2F

このモデルのonnxが公開されているのでonnxruntimeを使用して、TouchDesigner上で動かしてみようと思います。

### onnxruntimeとは
onnxruntimeとはDeepLearningとして学習されたモデルを動かすためのライブラリ(推論エンジン)のようなものです。

onnxに変換されたあらゆる学習モデルはonnxruntime上で動かすことができます。さらに、onnxruntimeはWindows, Mac, Linux, Android, iOSに対応しているので、onnxに変換されたモデルは実質的にどのデバイスでも実行できるようになります。（ただし、現実には性能要件などに制限されます。）

また、CUDAなどに対応しているonnxruntime-gpuもあるので、GPUの力を借りて高速に動かせることも強みです。

さらに、onnxruntimeはC++, C#, Pythonなどから利用できるため、使いやすいことも特徴です。

今回は、Python上からonnxruntimeを利用できるようにし、さらにTouchDesigner上でそのPythonを動かしたいと思います！

### pyenvとvenvを使用する理由
pyenvとは、Pythonのバージョンを切り替えられる仕組みです。
また、特定のバージョンのPythonを導入するのにコマンド一発でインストールできるため便利です。今回は、TouchDesigner上で動いているPythonのバージョンと揃える必要があるため、利用します。


venvとは、virtual environment、仮想環境を作る仕組みです。
Pythonで使用するライブラリ(numpyやonnxruntimeなど)をどかっと揃えられます。さらに、プロジェクトごとに使用するライブラリ環境を切り替えられるため、複数のonnxを走らせたいときや違うTouchDesignerに競合を発生させないために重宝します。

## python(pyenv + venv)導入
### pyenvを入れる



### venvを入れる
