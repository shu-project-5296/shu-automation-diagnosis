# SHU AUTOMATION 無料診断LP

一般公開用にSNS管理画面から分離した、無料セルフ診断LPです。

- 静的フロントエンド（`index.html` / `styles.css` / `app.js`）
- Cloudflare Pages Functionsによる診断イベント記録
- UTMクエリと`landing_variant`を画面遷移中も保持
- SNS管理画面、Secrets、顧客データは含みません

## Cloudflare設定

Pagesプロジェクトへ接続し、既存D1を`DB`というBinding名で設定してください。計測先テーブルは既存の`diagnosis_daily_stats`を使用します。

GitHub Pagesだけで公開した場合、画面は動作しますがPages FunctionsとD1計測は動作しません。計測を維持する本番公開にはCloudflare Pagesを使用してください。
