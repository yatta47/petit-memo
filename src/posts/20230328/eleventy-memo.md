---
title: Eleventyのメモ
date: '2023-03-28'
slug: 20230328-memo
tags: [eleventy]
description: 今日調べたもの
permalink: posts/{{ date }}-{{ slug }}/index.html
---

{{ description }}

## EleventyのTheme

前々から作りたかったEleventyのページを作成。

テンプレートを色々調べて、以下のサイトから選んだ。

[Eleventy Themes (31)](https://jamstackthemes.dev/ssg/eleventy/)

[23 of the best Eleventy Themes (Starters) for 2023 | CloudCannon](https://cloudcannon.com/blog/23-of-the-best-eleventy-themes-for-2023/)

結果的に以下のテンプレートを使用することにした。

[yinkakun/eleventy-duo: Eleventy Duo is a minimal and beautiful Eleventy theme for personal blogs.](https://github.com/yinkakun/eleventy-duo)

このテンプレートも捨てがたかったが何となく白ベースでシンプルなものってことで上のやつを選びました。

[arpitbatra123/eleventy-blog-mnml: A minimal blog template using eleventy](https://github.com/arpitbatra123/eleventy-blog-mnml)

## yarnが実行できない

yarnコマンドを打ったら以下のエラーが出た。

```command
$ yarn
nodenv: yarn: command not found
```

原因的にはnodenvでnodeを管理している場合にyarnが入っていないらしいので、追加で入れることで対応。

```command
sudo su -
npm install --global yarn 
```

自分の場合はrootでnodenv入れているのでrootユーザで実行した。

参考サイト：[nodenv: yarn: command not foundがでたときにyarnを入れる方法 – Tech Blog](https://techblg.app/articles/how-to-install-yarn/)

## yarn devでエラー

ログでエラー文言が消えちゃったのでどんなエラーが出たのか忘れちゃったんだが、残っている限りだとyarn dev時に以下のエラーが発生。

```shell
error:03000086:digital envelope routines::initialization error
```

以下のサイトを参考に対応。

[Node.js 17以上にした際のOpenSSL互換エラー対応](https://zenn.dev/yogarasu/articles/425732ff408d06)
