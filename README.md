![投稿](https://user-images.githubusercontent.com/73045514/116842216-c5a33e80-ac16-11eb-93a6-c3ddc06b8c77.jpg)

## プロジェクト名 SHALIBO

https://shalibo.netlify.app/

Qiita にも執筆しました。
[Vue.js、FireBase で読書管理アプリを作ってみた](https://qiita.com/oga0927/items/abf48b692b11fec6ae36)

## 概要

本の内容が要約されたまとめアプリです。

読んで学んだことをアプリの質問に応じて記述するとアウトプットになります。GoogleBookApi を使って本を検索することができます。マイページで投稿した本の要約を読み返すこともできます。投稿した本はトップページで表示され、ログイン中のアカウントと紐づいた本を編集、削除することが可能です。投稿した本の情報を共有することもできます。他の方が要約して投稿した本を見ることもできます。購入する際の参考にもなります。スマートフォン用にレスポンシブ対応しています。

## 制作背景

購入前に『どんな本だったか知りたい』、『本の内容をアウトプットしたい』、『要約された本の内容を知りたい』、『読む時間を短縮したい』、『本を持ち歩かなくても本の内容をいつでも振り返りたい』と思った背景から開発しました。

## 使用技術

- フロントエンド

  - Vue.js
  - VueRouter
  - Vuex
  - Vuetify

- バックエンド

  - Firebase(Authentication)
  - GoogleBookAPI / WebStorage(LocalStorage)

- サーバー
  - Netlify

## 機能一覧

- 認証機能

  - ユーザー登録
  - ログイン機能
  - ログアウト機能
  - アカウント削除機能

- CRUD 機能

  - 本のタイトル検索
  - 本の投稿機能
  - 投稿内容編集機能
  - 本の削除機能
  - 詳細一覧機能

## 使い方

- ユーザー登録にアクセスすると、登録画面に切り替わるのでユーザーネーム、e-mail、パスワードを入力して登録ボタンを押します。（ユーザーネームを入力しない場合はゲストログイン名として表示されます）
- 既にアカウントをお持ちの場合は フォームに e-mail とパスワード入力でログインすることができます。
- 『おすすめの一冊を投稿』ボタンを押すと本の検索画面に遷移するので、本のタイトルを入力して検索ボタンを押すと、GoogleBookApi から取得されたキーワードで一致した本が最大４０件表示され、検索結果から投稿したい本を選択できます。
- 検索結果で表示されている本の＋ボタンを押すと『読んだ日付』、『この本にはどんな情報が書かれているか』、『自分はこの本から何を学んだか』、『この本がなぜ重要なのか』、『テーマに対しどのような事例を出しているか』、『この本が他の本と似ている所、違う要素は何か』を入力して投稿ボタンを押すと投稿できます。
- 投稿した本とユーザー id が紐づいており、他のユーザーが書き込めないように投稿リストにはログイン中のユーザー id と紐づいた本のみ削除、投稿ボタンの表示非表示されます。
- 投稿した本の削除ボタンを押すと、アラートでメッセージが表示され、OK ボタンを押すと LocalStorage から該当する本のデータが削除されます。
- ヘッダーのロゴ（SHALIBO）を押すとトップページへリダイレクトされます。

## テスト用アカウント <br>

username: test <br>
E-mail: shalibo@test.com <br>
Password: password

## ライセンス

- GitHub: https://github.com/oga0927/Book_Library_Vue.js
- URL: https://shalibo.netlify.app/

[![Netlify Status](https://api.netlify.com/api/v1/badges/afd7c925-e94a-4341-8f10-3161df0ddda0/deploy-status)](https://app.netlify.com/sites/shalibo/deploys)
