## Golangで
## MiniLispを作ってみた
### 0x64物語 Reboot \#09
### @otakumesi

---

## みなさん、木といったらなにを思い浮かべますか？

---

## クリスマスツリー、木構造、二分木、...

---

# Lisp

---

## Lisp
カッコが多いとかで敬遠されがちな言語。  
マスコットキャラのLispエイリアンが可愛い。  
Haskell共和国と戦争中らしい（某書によると）  
<font color="red">LIS</font>t <font color="red">P</font>rocessorを略した名称に由来。  

---

## Lispエイリアン

![lispエイリアン_1](./imgs/lisplogo_alien_256.png)
![lispエイリアン_2](./imgs/lisplogo_warning_256.png)
![lispエイリアン_3](./imgs/lisplogo_256.png)

---

## Lispの構文は木構造
簡単なLispのコードを見てみましょう。
```lisp
(+ (* 1 (+ 3 4)) (- 5 (/ 10 5)))
;; => 10
```

---

## Lispの構文は木構造
ちゃんとインデントをつけてみてみると、  
木構造に見えてきませんか？
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
Lispの構文のS式はそのまま構文木になります

<pre style="width: 130px;display:inline-block;"><code class="lang-lisp hljs"><span class="line">(<span class="hljs-name">+</span></span><span class="line">  (<span class="hljs-name">*</span> <span class="hljs-number">1</span></span><span class="line">    (<span class="hljs-name">+</span> <span class="hljs-number">3</span> <span class="hljs-number">4</span>))</span><span class="line">  (<span class="hljs-name">-</span> <span class="hljs-number">5</span></span><span class="line">    (<span class="hljs-name">/</span> <span class="hljs-number">10</span> <span class="hljs-number">5</span>)))</span><span class="line"><span class="hljs-comment">;; =&gt; 10</span></span></code></pre>

<pre style="width: 130px;display:inline-block;">
     +
   /   \
  *     -
 / \   / \
1   +  5  ÷
   / \   / \
  3   4 10  5
</pre>

---

# GolangでLispを
# 実装した話

---

## 動機

- Golangを学び始めてたので良い題材が欲しかった
- (元)Emacs使いとしての目標の一つだった
- 0x64物語のお題が「木」だった

---

## デモ（REPL）

![lispon](./imgs/lispon.gif)

---

## 感想

書き始めは演算子オーバーロードとかジェネリックが欲しいなとか、  
生粋のGopherの目の前で言ったら後ろから刺されそうな文句をブツブツ言ってました。

---

## 感想

でも、Goを書いてるといつの間にか心地よくなってきて、そんなことどうでもよくなりました（？）

---

## せっかくなのでHTMLを書いてみた
![](./imgs/lisphtml.png)

---

Golang経由でLambdaから  
Lispで書いたHTMLでHelloWorldした図（？）

![](./imgs/helloworld.png)

---

これをツイートしたらmattnさんにRTされて、  
こんなコメントを貰えたので僕は満足しました

---

# 終わり

![](./imgs/daretoku.png)
