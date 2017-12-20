# 小さなLispインタプリタを作ってみた
## 0x64物語 Reboot \#09
## @otakumesi

---

## みなさん、木といったらなにを思い浮かべますか？

---

## クリスマスツリー、木構造、二分木、...

---

<center>

# Lisp

</center>

---

## Lisp
<font color="red">LIS</font>t <font color="red">P</font>rocessorを略した名称に由来しています。  
その名の通りリスト処理が得意な言語です。

---

## Lispの構文は木構造
簡単なLispのコードを見てみましょう。
```lisp
(+ (* 1 (+ 3 4)) (- 5 (/ 10 5)))
;; => 10
```

---

## Lispの構文は木構造
ちゃんとインデントをつけてみてみると、木構造に見えてきませんか？
```lisp
(+
  (* 1
    (+ 3 4))
  (- 5
    (/ 10 5)))
;; => 10
```

---

## Lispの構文は木構造
Lispの構文のS式はそのまま構文木になる
<pre>

     +
   /   \
  *     -
 / \   / \
1   +  5  ÷
   / \   / \
  3   4 10  5

</pre>

---

# Lispを実装してみた話

---

# 開発に使った言語
<center>

![Golang](/Users/otakumesi/Documents/0x64-reboot-tree-slide/imgs/gopher-side_color.png)
</center>

---

# デモ（REPL）

![lispon](./imgs/lispon.gif)

---

# 感想


---

# せっかくなのでHTMLを書いてみた
![](/Users/otakumesi/Desktop/スクリーンショット%202017-12-03%2012.34.47.png)

---

# Apex（Golang）を使ってAWS LambdaからLispでHelloをWorldした図（？）

![](/Users/otakumesi/Desktop/スクリーンショット%202017-12-03%2012.34.00のコピー.png)

---

# これをツイートしたらmattnさんにRTされた

![](/Users/otakumesi/Desktop/daretoku.png)
