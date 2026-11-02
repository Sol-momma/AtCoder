[English](README.md) | [日本語](README.ja.md)

# AtCoder

AtCoder の練習用リポジトリです。C++ の開発環境と AtCoder Library を置いています。

[AtCoder](https://atcoder.jp/) のコンテスト向け C++ 練習用ワークスペースです。公式の [AtCoder Library (ACL)](https://github.com/atcoder/ac-library) を同梱しているので、追加のセットアップなしで `#include <atcoder/all>` できます。

## 内容

```text
.
├── ac-library/      # AtCoder Library: headers (atcoder/), docs (document_en, document_ja), expander.py
└── test.cpp         # minimal program to check the compiler setup
```

## 使い方

同梱ライブラリをインクルードパスに入れて解答をコンパイルします。

```sh
g++ -std=c++17 -O2 -I ac-library test.cpp -o a.out
./a.out
```

AtCoder は単一のソースファイルを受け付けます。提出前に、使っている ACL ヘッダを1ファイルへ展開するには次を実行します。

```sh
python3 ac-library/expander.py main.cpp   # writes combined.cpp
```

ライブラリのドキュメントは `ac-library/document_en/index.html`（英語）と `ac-library/document_ja/index.html`（日本語）にあります。

## 技術スタック

- C++17（g++ または clang++）
- AtCoder Library
- Python 3（`expander.py` のみ）

## ライセンス

`ac-library/` のコードは AtCoder Library であり、独自のライセンス [ac-library/atcoder/LICENSE](ac-library/atcoder/LICENSE)（CC0）で配布されています。このリポジトリのそれ以外にはライセンスファイルがないため、著作者がすべての権利を留保します。
