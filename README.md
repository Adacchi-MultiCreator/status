# サービス稼働状況ページ

Adacchi Creative の Blender アドオンの、ライセンス認証・申請の稼働状況を公開するページです。
GitHub Pages で `https://status.adacchi-creative.com/` に公開します。

## しくみ

- 見た人のブラウザが、ライセンスサーバーの公開用の状況 API（`/api/v1/public-status`）を読み、○ / △ / × を表示します。
  サーバーにつながらないときは、ページが自動で「×（接続できません）」を表示します。
- 過去90日の稼働と稼働率は、外部監視の Upptime（`Adacchi-MultiCreator/upptime`）が記録した `history/summary.json` から読みます。
- お知らせ（メンテナンス・障害など）は、ライセンス管理画面の「サービス状況」から登録します。

## 設定

`index.html` の先頭近くにある `CONFIG` だけを書き換えます。

| 項目 | 内容 |
|---|---|
| `apiUrl` | ライセンスサーバーの状況 API |
| `upptimeSummaryUrl` | Upptime の集計データ |
| `upptimeSiteUrl` | 「詳しい稼働履歴」のリンク先 |
| `upptimeSlug` | Upptime の監視のうち、ライセンスサーバー本体のもの |
| `contactUrl` | 「お問い合わせ」のリンク先 |
