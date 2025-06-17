# プロジェクトの使い方

このドキュメントでは、`cilantro` ライブラリのビルド方法と、付属するサンプルコードの実行方法を説明します。

## 必要なソフトウェア

- [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page) 3.3 以降（必須）
- [Pangolin](https://github.com/stevenlovegrove/Pangolin) （オプション、例の多くで使用）
- [CMake](https://cmake.org/) 3.0 以降

## ビルド手順

1. リポジトリを取得します。
   ```bash
   git clone https://github.com/kzampog/cilantro.git
   cd cilantro
   ```
2. ビルド用ディレクトリを作成して CMake を実行します。
   ```bash
   mkdir build
   cd build
   cmake ..
   make -j
   ```
   以上でライブラリとサンプルがコンパイルされます。

## サンプルコードの実行

サンプルは `build/examples` ディレクトリに配置されます。多くのプログラムは点群ファイル（PLY 形式）へのパスを引数として受け取ります。リポジトリには `examples/test_clouds/test.ply` が用意されているため、以下のように実行できます。

```bash
./build/examples/kmeans ../examples/test_clouds/test.ply
```

他の実行ファイルでも同様に、第一引数に PLY ファイルを指定してください。引数が足りない場合は、プログラムが使い方を表示します。

