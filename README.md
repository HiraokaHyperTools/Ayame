# Ayame

[![The MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

[http://ayame.solunita.net/](http://ayame.solunita.net/)

[![Honoka](docs/img/sample.png)](http://ayame.solunita.net/)

"Ayame" は"[Honoka](https://github.com/windyakin/Honoka)"を元に作られた、日本語を美しく表示することに特化したBootstrapテーマです。

## About "Ayame"

通常の[Bootstrap](http://getbootstrap.com/)では、日本語のフォント指定や文字サイズは最適とはいえません。"Honoka"はそんなBootstrapをベースに、日本語表示に適したフォント指定や、文字サイズに関するコードを追記したBootstrapテーマの一つです。

"Ayame"は"Honoka"を元に、ダーク系の配色を適用し、さらに行間やカーニング、日本語の表示によりこだわりました。
具体的には約物にYakuhanJPを使い、line-heightとletter-spacingを調整、vertical-rhythmを意識したブロック間のマージン、text-align: justify による均等割付、などが加えられています。

## Live Demo

 * [Ayame/bootstrap-ja.html](http://dev.solunita.net/ayame/bootstrap-ja.html) (日本語レイアウト)

## Getting Started

### Download

[Releases](https://github.com/AquiTCD/Ayame/releases)から最新版をダウンロードしてください。

#### 自身でカスタマイズしたり、ビルドする場合。
(Requirement: node.js, gulp)

```
git clone https://github.com/AquiTCD/Ayame.git
cd Ayame
yarn install #or $npm install
npm run deploy #or npm start
```

## Usage

Ayameは単なるBootstrapテーマにしか過ぎないため、基本的な使い方は"Honoka"に順じ、本家Bootstrapとほとんど変わりません。よって以下に書くことは[本家Bootstrap](http://getbootstrap.com/getting-started/)からの引用、もしくはその一部を変更したものです。用意されたCSSクラスやコンポーネントなど、より詳細な使い方のドキュメントは本家Bootstrapの各種リファレンスページをご覧になることを推奨します。

 * [CSS](http://getbootstrap.com/css/)
 * [Components](http://getbootstrap.com/components/)
 * [JavaScript](http://getbootstrap.com/javascript/)

### Package

<!-- 配布しているzipファイルの内容物は以下のとおりです。``bootstrap.min.*``といったように、ファイル名に``min``がつくファイルは、改行やインデント・スペーシングをなくした(minifyされた)コードで、ユーザがウェブページを読み込む際の転送量を少なくすることができます。通常はこの``bootstrap.min.*``を使うことをおすすめします。 -->

```
Ayame/
├── bootstrap-ja.html
├── css
│   ├── bootstrap.css
│   ├── example.css
│   └── plugins
│       └── yakuhanjp.min.css
├── fonts
│   ├── YakuHanJP-Black.eot
│   ├── YakuHanJP-Black.woff
│   ├── YakuHanJP-Black.woff2
│   ├── YakuHanJP-Bold.eot
│   ├── YakuHanJP-Bold.woff
│   ├── YakuHanJP-Bold.woff2
│   ├── YakuHanJP-DemiLight.eot
│   ├── YakuHanJP-DemiLight.woff
│   ├── YakuHanJP-DemiLight.woff2
│   ├── YakuHanJP-Light.eot
│   ├── YakuHanJP-Light.woff
│   ├── YakuHanJP-Light.woff2
│   ├── YakuHanJP-Medium.eot
│   ├── YakuHanJP-Medium.woff
│   ├── YakuHanJP-Medium.woff2
│   ├── YakuHanJP-Regular.eot
│   ├── YakuHanJP-Regular.woff
│   ├── YakuHanJP-Regular.woff2
│   ├── YakuHanJP-Thin.eot
│   ├── YakuHanJP-Thin.woff
│   ├── YakuHanJP-Thin.woff2
│   ├── glyphicons-halflings-regular.eot
│   ├── glyphicons-halflings-regular.svg
│   ├── glyphicons-halflings-regular.ttf
│   ├── glyphicons-halflings-regular.woff
│   └── glyphicons-halflings-regular.woff2
├── img
│   ├── ayame.png
│   ├── circle.png
│   └── sample.png
├── index.html
└── js
    ├── bootstrap.js
    └── bundle.jsush
```

### Basic Template

Bootstrapをつかってウェブページを作成する際に基本となるHTML部分は以下のようになります。CSSやJavaScriptのファイルパスは環境に合わせて変更する必要があります。

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Bootstrap 101 Template</title>

    <!-- Bootstrap -->
    <link href="css/bootstrap.min.css" rel="stylesheet">

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="js/bootstrap.js"></script>
  </body>
</html>
```

### Do you Love "YuGothic"?

Ayameではローカルに源ノ角ゴシック（≒Noto Sans CJK JP）があれば優先的に使用します。存在しない場合は使用環境に準拠した読み易いフォントが使われます。(Web-fontとして使用しないのは現状はパフォーマンスが良くないため避けました）
もしあなたが日本語フォントに游ゴシックを指定したい場合、その要素に対して`.i-love-yu`(※`you`ではなく`yu`)を指定することで游ゴシックの指定になります。

例えばページ全体に対して游ゴシックを用いたい場合は、`<body>`に対して`.i-love-yu`を指定(`<body class="i-love-yu">`)することで、ページ全体で游ゴシックが使用されます。
またAyameでは游ゴシックを使う際もOSやブラウザによる際をなるべく吸収するように設定されています。

## Build

```
yarn install
npm deploy
```

## Customize Tips
`gulpfile.ts`中の以下の設定で簡単に切り変えられる設定があります。
```ts:
useCDN = true
modeKurenai = true
```

### Use CDN
`bootstrap.min.css`(または`bootstrap.css`)以外をCDNを使いたい場合、`useCDN = true`にしてください。

### 紅モード
`modeKurenai = true`にするとプライマリーカラーが紅色になります。それにともない他の色も若干の調整が加わります。赤系の色が好きな人にお勧めです。

## License

[MIT License](LICENSE)

## Author of "Honoka"

- windyakin ([windyakin.net](http://windyakin.net/))

## Editor of "Ayame"

- AquiTCD ([Trial and Spiral](http://blog.solunita.net/))

## Fonts

- [Yaku Han JP](https://qrac.github.io/yakuhanjp/)
- [Google Noto Fonts](https://www.google.com/get/noto/)
