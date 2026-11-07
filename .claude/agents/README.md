# Claude Code サブエージェント

このリポジトリ（うちのこ手帳プレビュー）用のエージェント定義です。メインのClaudeが用途に応じて呼び出します。

| 名前 | モデル | 用途 |
|---|---|---|
| pwa-implementer | sonnet | manifest・Service Worker追加、不具合修正などの実装 |
| ui-mobile-checker | haiku | iPhone幅のレイアウト/操作性/アクセシビリティ点検（読み取り専用） |
| sale-readiness-reviewer | sonnet | ラッコM&A買い手目線の売却前レビュー（読み取り専用） |
| security-auditor | sonnet | 秘密情報・XSS・復元処理の監査（読み取り専用） |

## 並列利用の頼み方の例

> ui-mobile-checker、security-auditor、sale-readiness-reviewer を並列で動かして、結果を重要度順に1つにまとめて。

> 点検3つを並列で実行し、その結果を踏まえて pwa-implementer に manifest と Service Worker を追加させて。
