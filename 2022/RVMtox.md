
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
    2.　RVMに必要なライブラリを導入する
4. TouchDesignerにRVMの環境を適用させる
5. TD上でプログラムを書く
    1. TDからpythonに画像をおくる
    2. python上でRVMに適したデータ形式に整形する
    3. 結果をTDに送る
    4. Composite
