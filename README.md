# 今日100点？ サポートサイト

iOSアプリ「今日100点？」（`~/dev/omae-100ten`）のサポートサイト。
App Store Connectに登録するサポートURLとプライバシーポリシーURLになる。

ビルド不要の静的サイト。HTMLとCSSだけで、依存パッケージはない。

```
index.html          トップ
support/index.html  サポート（/support）
privacy/index.html  プライバシーポリシー（/privacy）
styles.css
icon.png            アプリと同じアイコン
```

## 連絡先

`support/` と `privacy/` に `moderate.app.support@gmail.com` を載せている。
取得済み。アプリ名ではなく公開名義（Moderate）で取ってあるので、今後出す
アプリでもそのまま使い回せる。

宛先を変えるときはこの2ファイルを書き換える。

```
grep -rn "moderate.app.support@gmail.com" .
```

## ローカルで見る

```
python3 -m http.server 8000
```

## デプロイ

静的ファイルを置けるところならどこでもよい。Cloudflare Pages / GitHub Pages /
Netlify など。リポジトリを繋いでビルドコマンドなし・出力ディレクトリをルートに
設定すれば公開できる。

公開後のURLを App Store Connect の「サポートURL」と
「プライバシーポリシーURL」に入れる。
