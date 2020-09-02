# ゼロから作る Deep Learning 3

## 概要

『ゼロから作る Deep Learning 3』を進めていく

## URL

- [オライリージャパン](https://www.oreilly.co.jp/books/9784873119069/)

## 躓いたポイント

### ステップ 40

step40.py でエラー

![](https://user-images.githubusercontent.com/61448492/91954804-46830100-ed3d-11ea-8e21-66731b012f97.jpg)

\_\_init\_\_.py の else 節に ```import dezero.functions``` を追加することで動くようになった

```
else:
    ...
    from dezero.core import setup_variable

    import dezero.functions
```
