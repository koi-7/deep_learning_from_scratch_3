# ゼロから作る Deep Learning 3

## 概要

『ゼロから作る Deep Learning 3』を進めていく

## URL

- [オライリージャパン](https://www.oreilly.co.jp/books/9784873119069/)
- [GitHub（オライリージャパン）](https://github.com/oreilly-japan/deep-learning-from-scratch-3)

## 躓いたポイント

### ステップ 40

\_\_init\_\_.py の else 節に ```import dezero.functions``` も加えておく

### ステップ 43

linear、sigmoid は functions.py にコピペしておく。さらに、dezero ディレクトリに cuda.py をつくって（コピペでよい）、function.py にて cuda をインポートする。

### ステップ 45

\_\_init\_\_.py の else 節に ```from dezero.layers import Layer``` も加えておく

### ステップ 48

テキストのコードだけではとても実行できないのでエラーを見ながらその都度コードを追加していく

### ステップ 49

datasets.py に get_spiral 関数を追加する必要がある
