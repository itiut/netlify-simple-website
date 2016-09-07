netlify-simple-website
====

A simple website hosted on netlify at http://itiut-netlify-simple-website.netlify.com

メモ
----

### プランの違い
#### free ~
- カスタムドメイン
- カスタムドメインでHTTPS
- jsスニペットを全ページに挿入

#### paid (basic ~)
- basic auth
- password protection （サイト全体）
- build-in form
- prerendering

### Continuous Deploymentについて
- production環境とするブランチ、ビルドコマンド、公開するディレクトリを指定
  - `Gemfile`や`package.json`などのdependenciesはビルド前によしなにインストールしてくれる
- プルリクエスト毎にdeploy-preview環境が作られる
  - （`netlify init`しておくと？）マージされたら自動でproduction環境にpublishされる
- GitHub, Bitbucket, Slackと連携可能
  - commit status notificationとpull request notificationでは、Deploy started, Deploy succeeded, Deploy failedの3つのイベント全てを設定しておくと良い
- テストは別のCIで行うのが良いと思われる
  
