# カスタマイズメモ

## ローカル化

[https://toha-guides.netlify.app/posts/](https://toha-guides.netlify.app/posts/)

- `Quickstart`で確認。すんなりOK。
- GitHub Pagesの設定をDeploy from a branchに変更。カスタムドメイン用に自動でCNAMEを作成するように追加。
- 色を編集したいのでvariables.scssをhugo-tohaからコピーして編集。

## ホームカスタマイズ

- レイアウト調整
  - [https://toha-guides.netlify.app/posts/customizing/customize-layout/](https://toha-guides.netlify.app/posts/customizing/customize-layout/)
  - layoutフォルダをコピー
  - variables.scssで文字間等を調整
  - Experienceの表示が気になるので修正　layouts/partials/sections/experiences/positions.html
    - 縦一直線化
    - タイトルとResponsibilitiesの間が狭いのでCSSで調整
    - 在籍期間を改行
    - 会社間の隙間をbootstrapで調整
    - ポジション間に水平線追加
  - Aboutの自己紹介文を左揃えに修正
  - Aboutに見出し追加
  - Experienceの年月がサファリだと電話番号と認識されるため、Month yyyyに変更

## コマンド

HTMLを出力。GitHubで公開するなら不要
hugo --minify

HUGOサーバーを立ち上げ。通常はこれで修正を確認する。
hugo server -D

新しくポストを作成する場合
hugo new posts/new-post.md

## 見た目を変える

- 文章等はdataフォルダの中身を修正
- そもそもの見た目をいじるならlayouts/partials/sectionsのHTMLを直接いじる
- 言語間で対応ワードの差異がたまにある