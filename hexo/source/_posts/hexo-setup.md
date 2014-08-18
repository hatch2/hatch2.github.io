title: hexoセットアップしてみた
date: 2014-08-16 08:34:24
tags: [hexo, node, github]
---
最近流行ってるらしいhexoという静的ページジェネレータをつかって何もやってなかったGithub PageにBlogを設置してみました。
第一印象としてはJekyllのnode版の様な感じで、テンプレートを記述するメタ言語を変更できたり、node moduleをつかって拡張したりできます。


## セットアップ
とりあえずnvmやnodebrewを入れてnodeの最新版をインストール(ここは別のサイトを調べていただいて)します。
nodeが入ってしまえば3ステップで始められます。

```bash
$ npm install -g hexo        # 1 hexoをインストールします
$ hexo init <プロジェクト名>   # 2 hexoのプロジェクトフォルダを作成します
$ npm install                # 3 hexoに必要なnode moduleのインストールをします
```

以下のサーバを立ち上げてみましょう。
ローカル上で実際に公開される記事をプレビューする事ができます。
通常の場合は http://localhost:4000/ をブラウザで開くと確認できます。

```bash
$ hexo s                     # hexoのサーバを起動する
```


## プラグインでやりたい事をやれるようにする
hexo用のnode moduleを追加する事でsassやcoffeeやjadeなどのメタ言語が利用できるようになります。
テンプレートなども変更できるようなので少しずつカスタムしてみようかと思います。
以下のページに利用できるテンプレートやnode moduleがリストになっているので使いたいmoduleをpackage.jsonに追加して```npm install```でインストールする事ができます。

- [Plugins · hexojs/hexo Wiki](https://github.com/hexojs/hexo/wiki/Plugins)

## 参考サイト
- [所要時間3分!? Github PagesとHEXOで爆速ブログ構築してみよう！ | 株式会社LIG](http://liginc.co.jp/web/programming/server/104594)
- [チームブログをGitHubとHexoではじめよう！ | Tokyo Otaku Mode Tech Blog](http://blog.otakumode.com/2014/08/08/Blogging-with-hexoio/)