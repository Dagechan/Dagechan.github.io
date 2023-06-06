---
title: "apt installのNeovimは古い！"
date: 2023-06-03T16:52:55+09:00
categories:
- Tech
- Linux
tags:
- Neovim
- Linux
- Ubuntu
- Vim
- WSL
keywords:
- tech
comments:       false
showMeta:       true
showActions:    false
#thumbnailImage: //example.com/image.jpg
---

　こんにちは．Dagechanです．今回はUbuntuにNeovimを導入しようと思います．
<!--more-->

--------------**ここからneovimの導入には関係ない前書き**----------------

私が所属している大学では，演習の際に大学側が用意した環境を取り込むわけですが，そこでの既定のテキストエディタがかなり質素なものでした．

私は「vscode使おう」と逆張りしたわけですが，やはり便利なものでとても使いやすい高機能なテキストエディタです．今でもたくさんお世話になっているわけですが，最近は大学の講義でもあまりその質素なエディタを推奨される機会が減り，vscodeを使った演習が多くなりました．つまりvscodeを使う学生が大多数になったわけです．そうなるとvscodeにも飽きてしまい，他に何か良いエディタがないものかと考えました．

そこで見つけたのがNeovimです．というのもこれを選んだ理由としては，某Youtuberの方がこれを使って開発しておられるのを見て，かっこいいと思ったからです（小並感）．

-----------------------------**ここまで**------------------------------

とりあえずUbuntuでNeovimを導入しようと思って以下のようにインストールしたわけです．

```bash
$ sudo apt install neovim
```
{{< figure src="/images/ubuntu-nvim.png" title="apt installで得たNeovim（画像大きくてすみません）" class="center" >}}

**<p>「NVIM v0.6.1」</p>**
古いです．今回私はマジのUbuntuにNeovimを導入していますが，この記事を書く前にWSL2で後に紹介するdein.vimをコマンドラインでインストールした場合，Neovimのバージョンが0.9.0以上でないと使えないとかいうエラーが出ました．どうやらapt installではダメみたいですね．．．そこでsnapを使って以下のようにインストールしたら，ちゃんとv0.9.0をインストール出来ていました．

```bash
$ sudo snap install nvim --classic --stable
```
classicオプションは，classic confinementを意味しており，これがないとNeovimがsnapでインストール出来ませんでした（詳しいことは今のところまだ理解していない）．stableオプションは安定版をインストールするためのオプションです．

{{< figure src="/images/ubuntu-nvim2-1.png" title="snap installで得たneovim" class="center" >}}

ちゃんとV0.9.0になっています．やったぜ．


<P>そしてNeovimのプラグインマネージャとしてdein.vimを導入しました．</P>
<p>（下記公式ドキュメントを参考にした↓）</p>
<p>https://github.com/Shougo/dein.vim</p>

拙い文章で知識もまだまだですが，これからもつらつらと書いていこうと思います．














