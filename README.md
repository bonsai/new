# bonsai/new

Synced Repos — ローカルから削除された GitHub リポジトリのライブフィード

## https://bonsai.github.io/new/

`repos.sqlite` の `status='deleted'` レコードを JSONL として配信。
GitHub Pages でリアルタイム表示（5秒ポーリング）。

## 更新タイミング

`sync-repos` ワークフローがローカル削除を実行したタイミングで `data.jsonl` が更新される。

## フィールド

| field | 説明 |
|-------|------|
| folder_name | ローカルフォルダ名 |
| github_url | GitHub URL |
| diff_status | identical / local_ahead / remote_ahead / diverged |
| similarity_score | 近似度 (0.0〜1.0) |
| deleted_at | ローカル削除日時 |
