# map-sync-scheduler

このリポジトリで運用していた GitHub Actions ベースのUR同期schedulerは廃止しました。

現在の定常同期は `ur-life-map/ur_life_map` の `apps/ur-sync` を正本とし、Cloudflare Cron + Workers + Queues + ops D1 + R2 で完結します。

旧 `hourly-sync.yml` / `monthly-master-sync.yml` は再利用しないでください。同期の実行・監視・管理機能は Cloudflare 側の Sync Worker / Ops API に追加します。
