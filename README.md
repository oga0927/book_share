## プロジェクト名

SHALIBO

## 概要

本の内容が要約されたまとめアプリです。

読んで学んだことをアプリの質問に応じて記述していくことでアウトプットになります。マイページで投稿した本の要約を読み返すこともできます。投稿した本の内容はリスト化され、情報を共有することもできます。他の方が要約して投稿した本を見ることもできます。購入する際の参考にもなります。スマートフォン用にレスポンシブ対応しています。

## 制作背景

本の内容が要約された読書管理アプリがあればいいと思ったのと、購入前にどんな本だったか知りたい、本の内容をアウトプットしたい、要約された本の内容から読む時間を短縮したい。そんなアプリがあったらいいなと思った背景から開発に至りました。

## 使用技術

- フロントエンド

  - Vue.js を用いたシングルページアプリケーション
  - Vuex で状態管理
  - Vuetify でデザイン作成、レスポンシブ対応

- バックエンド
  - Firebase の Authentication でユーザー認証機能（ログイン、ログアウト、ユーザー登録、削除）
  - GoogleBookApi / WebStorage(LocalStorage)

## 使い方

- ユーザー登録にアクセスすると、登録画面に切り替わるのでユーザーネーム、e-mail、パスワードを入力して登録ボタンを押します。（ユーザーネームを入力しない場合はゲストログイン名として表示されます）
- 既にアカウントをお持ちの場合は e-mail とパスワードをフォームに入力するとログインすることができます。
- 『おすすめの一冊を投稿』ボタンを押すと本の検索画面に遷移するので、本のタイトルを入力して検索ボタンを押すと、GoogleBookApi から取得されたキーワードに一致した本が最大４０件表示されて検索結果から投稿したい本を選択できます。
- 検索結果で表示されている本の＋ボタンを押すと『読んだ日付』、『この本にはどんな情報が書かれているか』、『自分はこの本から何を学んだか』、『この本がなぜ重要なのか』、『テーマに対しどのような事例を出しているか』、『この本が他の本と似ている所、違う要素は何か』を入力して投稿ボタンを押すと投稿できます。
- 投稿した本とユーザー id が紐づいており、他のユーザーが書き込めないように投稿リストにはログイン中のユーザー id と紐づいた本のみ削除、投稿ボタンの表示非表示される。
- 削除ボタンを押したときはアラートでメッセージが表示されて、削除する場合は OK ボタンを押す。
-
-

##　テスト用アカウント
username: test
E-mail: shalibo@test.com
Password: password

##　ライセンス
https://github.com/oga0927/Book_Library_Vue.js
