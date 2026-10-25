# AtCoder

AtCoder の練習用リポジトリです。C++ の開発環境と AtCoder Library を置いています。

A practice workspace for [AtCoder](https://atcoder.jp/) contests in C++. It bundles a copy of the official [AtCoder Library (ACL)](https://github.com/atcoder/ac-library) so solutions can `#include <atcoder/all>` without extra setup.

## Contents

```text
.
├── ac-library/      # AtCoder Library: headers (atcoder/), docs (document_en, document_ja), expander.py
└── test.cpp         # minimal program to check the compiler setup
```

## Usage

Compile a solution with the bundled library on the include path:

```sh
g++ -std=c++17 -O2 -I ac-library test.cpp -o a.out
./a.out
```

AtCoder accepts a single source file. To inline the ACL headers you use into one file before submitting, run:

```sh
python3 ac-library/expander.py main.cpp   # writes combined.cpp
```

The library documentation is in `ac-library/document_en/index.html` (English) and `ac-library/document_ja/index.html` (Japanese).

## Tech stack

- C++17 (g++ or clang++)
- AtCoder Library
- Python 3 (only for `expander.py`)

## License

The code in `ac-library/` is the AtCoder Library and is distributed under its own license, [ac-library/atcoder/LICENSE](ac-library/atcoder/LICENSE) (CC0). The rest of this repository has no license file, so all rights are reserved by the author.
