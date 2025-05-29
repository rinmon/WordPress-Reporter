# WordPress 設定情報抽出ツール

WordPressサイトの設定情報を抽出し、HTMLレポートを生成するクライアントサイドツールです。このツールは完全にブラウザ内で動作します。

## バッジ
<!-- このバッジは、最初のリリース/タグがプッシュされ、GitHub上でタグからリリースが作成された後に有効になります。 -->
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/rinmon/WordPress-Reporter)](https://github.com/rinmon/WordPress-Reporter/releases/latest)
<!-- ライセンスを選択した場合は、ここにライセンスバッジを追加してください -->
<!-- 例: [![GitHub license](https://img.shields.io/github/license/rinmon/WordPress-Reporter)](https://github.com/rinmon/WordPress-Reporter/blob/main/LICENSE) -->

## 主な機能
- REST API経由で様々なWordPress設定を抽出します:
    - 一般設定、表示設定、ディスカッション設定、メディア設定、パーマリンク設定
    - 有効なプラグイン一覧
    - 有効なテーマ情報
    - ユーザー一覧と権限グループ
    - (ウィジェットとメニューは、現在REST APIの制限によりサポートされていません)
- 抽出されたデータのダウンロード可能なHTMLレポートを生成します。
- 完全にクライアントサイドで動作します。データは対象のWordPressサイト以外のサーバーには送信されません。
- ユーザー認証情報はメモリ内で処理され、使用後に破棄されます。

## 使い方
1.  **ダウンロード:** このリポジトリから `index.html` ファイルを取得します。
2.  **開く:** `index.html` ファイルを直接ウェブブラウザ（例: Chrome, Firefox, Edge）で開きます。
3.  **認証情報を入力:**
    *   WordPressサイトの完全なURL（例: `https://example.com`）を入力します。
    *   WordPressのユーザー名またはアプリケーションパスワードのユーザー名を入力します。
    *   WordPressのパスワードまたはアプリケーションパスワードを入力します。
4.  **データ抽出:** 「ログインして抽出開始」ボタンをクリックします。ツールがWordPressサイトからデータを取得します。
5.  **レポートをダウンロード:** 抽出が完了すると、概要が表示されます。「HTMLをダウンロード」ボタンをクリックしてレポートを保存します。

## 依存ライブラリ
このツールはCDN経由で以下のライブラリを使用しています:
-   [React](https://reactjs.org/)
-   [ReactDOM](https://reactjs.org/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [Babel Standalone](https://babeljs.io/docs/en/babel-standalone) (ブラウザでのJSXトランスパイル用)
-   [jsPDF](https://parall.ax/products/jspdf) (注意: 当初PDF生成を計画していましたが問題が発生したため、現在の主要な出力はHTMLです。jsPDFライブラリは引き続きリンクされています。)

## 互換性
-   最新のデスクトップブラウザで動作するように設計されています:
    -   Google Chrome
    -   Mozilla Firefox
    -   Microsoft Edge
-   macOSおよびWindowsでテスト済みです。

## 開発者向け情報
- アプリケーションは単一の `index.html` ファイルです。
- 対象サイトでWordPress REST APIが有効化され、アクセス可能である必要があります。基本認証またはアプリケーションパスワードが使用可能であるべきです。

## ライセンス
ライセンスを指定したい場合は、`LICENSE`ファイルを追加してください（例: MITライセンス）。
