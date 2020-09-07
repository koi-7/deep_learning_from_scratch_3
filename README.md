# ゼロから作る Deep Learning 3

## 概要

『ゼロから作る Deep Learning 3』を進めていく

## URL

- [オライリージャパン](https://www.oreilly.co.jp/books/9784873119069/)
- [GitHub（オライリージャパン）](https://github.com/oreilly-japan/deep-learning-from-scratch-3)

## 注意点

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

### ステップ 51

ステップ 48 同様、エラーを見ながら適宜コードをコピペしてくる必要がある

### ステップ 52

functions.py の一部書き換えが必要かもしれない（コメントアウトの箇所）

``` python
class ReLU(Function):
    def forward(self, x):
        # xp = dezero.cuda.get_array_module(x)     ## dezero. が不要
        xp = cuda.get_array_module(x)
        y = xp.maximum(x, 0.0)
        return y

    def backward(self, gy):
        x, = self.inputs
        mask = x.data > 0
        gx = gy * mask
        return gx
```

### ステップ 57

step57.py 後半の

``` python
y = F.conv2d_simple(x, W, b=None, stride=1, pad=1)
```

は transpose() のせいでうまく動かないので代わりに

``` python
y = F.conv2d(x, W, b=None, stride=1, pad=1)
```

にしていろいろ書き加える必要がある。

### ステップ 58

vgg16.npz は 490MB あり、ダウンロードに時間がかかる
