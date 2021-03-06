# RDプログラミングハンズオン サンプルプログラム.

## これはなんですか？
教育用に jonhoo/tetris-tutorial にあったテトリスのプログラムをフォークしてカスタマイズしてみました。
このリポジトリにはいくつかブランチがあり、それぞれ欠陥や追加要件があります。
masterブランチは jonhoo氏が作成したオリジナルのプログラムが稼働します。
(一部、教育用にコード内のコメントを翻訳したり、追加したりしています)
好きなブランチに切り替える事で、欠陥を修正したり、追加要件の実装にチャレンジが出来る・・・という試みです。



## 使い方

各開発環境からこのリポジトリをクローンして使ってみてください。

```bash
# git clone https://github.com/killinsun/RD-pg-tetris-tutorial
```

- Cloud9を使っていれば、クローンしたディレクトリ内の「index.html」を開いて[Preview] -> [Preview File index.html]を選択する事で、Cloud9上でプログラムが動きます（厳密にはブラウザに読み込んでいますが)

### ブランチを切り替えてお題に挑戦する

```bash
# git branch -a 
* master
  remotes/origin/001
  remotes/origin/001-answer
  remotes/origin/HEAD -> origin/master
  remotes/origin/master

# git checkout [ブランチ名]

# git checkout remotes/origin/001 //example
```

お題の内容は各自に配布した資料を確認してください。(予定)

### 答えを見る

各お題番号の後ろに「-answer」をつけると、答えの例が実装された
コードのブランチに切り替える事が出来ます。

```bash
# git checkout remotes/origin/001-answer //001の答えのブランチ
```

gitの機能で、お題と答えの差分が簡単にわかるチートを使いたいですか？

```bash
# git diff remotes/origin/001 remotes/origin/001-answer //答えではどのように書いたのか差分を表示
```

### お題の内容は残したまま、お題に挑戦したい（日本語不自由)
お題に挑戦する際、オリジナルのコードに変更を加えたくない事があると思います。
そんな時は作業用のブランチを作りましょう。

```bash
# git checkout remotes/origin/001  //001に挑戦する
# git checkout -b 001-work //ソースコードを弄りたいのでブランチを作成してみる
# touch hoge.txt    //ソースコードを弄る 
# git add . 
# git commit -m "001に挑戦した"
# git checkout remotes/origin/001 //オリジナルのソースコードのブランチ戻る
# git checkout 001-work //編集したソースコードのブランチに戻る
```

以下、オリジナルのREADME.md

---


## The story

My step-brother was playing Tetris today, but was getting annoyed about all the
ads and the "recharge time" in the game, and vented his frustration to me.
After pointing out that there are probably thousands of completely
frustration-free (well, apart from the gameplay) Tetris clones out there, I
jokingly told him to go write his own Tetris game instead. His immediate
reaction was "I could never do that". After some interrogration, he revealed
that he actually thought that doing so could be quite fun, if only there was a
good way for him to learn how to do so without studying Computer Science for
years. This is my attempt to make that possible.

## The game

If all you want to do is play Tetris, there is a working implementation in the
root of this repository which you can launch by clicking <a href="https://rawgit.com/jonhoo/tetris-tutorial/master/index.html" target="_blank">this link</a>. It even implements the [Super Rotation
System](http://tetris.wikia.com/wiki/SRS) correctly, if you care about that.
It's quite rudimentary (no levels, no sound, no "next piece", etc.), but fully
playable, and quite small.

## The tutorial

The meat of this repository is in [doc/](doc/), which holds all the tutorial
text. You start with the [intro](doc/intro.md), and follow the links from
there. I attempt to cover everything from the very basics (what is a variable?)
to how to build a complete, working Tetris game, so it is (/will be) quite
long, but hopefully it will be a good primer for those trying to get into
programming, but who find "introduction to JavaScript" style tutorials
completely uninteresting.

## Progress

The tutorial is far from finished, but at least the code is there. I'll be
writing on this when I have time, and I have many things to do, so I make no
guarantees about when new content will be added, nor when (if ever) the entire
tutorial will be completed. It's fun to write though, and if people seem to be
getting something out of it, I'm more inclined to continue.

## Feedback

Yes please! Open an issue using the GitHub [issue
tracker](https://github.com/jonhoo/tetris-tutorial/issues), send a [pull
request](https://github.com/jonhoo/tetris-tutorial/pulls) with improvement
suggestions, or just send me an [email](mailto:jon@thesquareplanet.com).
I'm not hard to get a hold of.
