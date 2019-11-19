# CakePHP_Web Test System

『テスト問題システム(仮)』<br>
cakePHP 3系で作成した、問題/回答の登録〜テスト〜自動採点できるWebアプリケーション。

## 概要

実装のメインはログイン認証とCRUD機能です。<br>

* ログイン機能
* 問題/答えの登録・編集・削除機能
* 問題の回答、自動採点機能
* 過去の採点結果の閲覧機能<br>

bakeコマンドは使用せずMVCを作成。

## 作業環境
 
使用PC: MacBook<br>
VirtualBox・Vagrantを使ってLAMP環境を構築・検証。

* CentOS: 7.4
* Apache：2.4
* MySQL：5.6
* PHP：7.3

## 技術選定

比較的使われている頻度の高い環境を選択。
* cakePHP3系、上記「作業環境」、DB
* Github・ChatWorkのツールを用いてエンジニア に質問・レビューしやすい環境であること。
* 公式ドキュメント、文献、Qiitaやブログ記事など、検索元は容易であること。

## コード作成ルール

レビューにあたり以下のルールを設定しました。

* 変数の統一。※アッパーキャメルは不可。<br>
キャメルケース…コントローラ・view側<br>
スネークケース…グローバル変数　<br>
*  必要に応じて、定数化した方がいい部分は定数化する。
* 使用されていない引数が設定されていないこと。
* 配列の書き方を統一。※基本的に(array)ではなく、[]で記載。
* 使いまわしていない変数は変数にせずそのまま使用する。
*  usersテーブルのdelete_flagはmysql側でデフォルト0を設定。

## 残作業

以下は今後の改修内容です。

* ユーザー認証の設定。
* 変数・配列・コメントアウトの見直し。
* 「問題と答えの確認・登録」ボタンで、登録数が0の場合は、一覧でなく登録画面に遷移する仕様にする。
* 回答欄が最大3件の表示になっているが、追加ボタンで欄数を増せる仕様にする。
* フロント側の検討。(現状テンプレートエンジンのみ)
