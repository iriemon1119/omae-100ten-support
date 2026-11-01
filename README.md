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

## 公開する前にやること

**連絡先メールアドレスを作る。** いま `support/` と `privacy/` に書いてある
`omae100ten.app.support@gmail.com` はまだ存在しない。
ポモテクと同じようにアプリ専用のGmailを取得するか、別の宛先に書き換える。
個人のメールアドレスをそのまま載せると公開先から拾われるので避けたほうがいい。

```
grep -rn "omae100ten.app.support@gmail.com" .
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
