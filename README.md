# SHU AUTOMATION 無料診断LP

一般公開用にSNS管理画面から分離した、無料セルフ診断LPです。

- 静的フロントエンド（`index.html` / `styles.css` / `app.js`）
- Cloudflare Pages Functionsによる診断イベント記録
- UTMクエリと`landing_variant`を画面遷移中も保持
- SNS管理画面、Secrets、顧客データは含みません

## Cloudflare設定

Pagesプロジェクトへ接続し、`PRIVATE_ANALYTICS_ORIGIN`と`SITE_BYPASS_TOKEN`をサーバー側環境変数として設定してください。公開LPの計測APIが所有者限定SNS OSの既存計測APIへ安全に中継します。

GitHub Pagesだけで公開した場合、画面は動作しますがPages Functionsと既存D1計測は動作しません。計測を維持する本番公開にはCloudflare Pagesを使用してください。
