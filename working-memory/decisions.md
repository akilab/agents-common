# Decisions

- 2026-08-09: `AGENTS.md` / `CLAUDE.md` は、特定のプロジェクト・技術スタック・組織固有の運用に依存させず、端末変更時にもそのままコピーして使える汎用指示として設計する。個別事情は各プロジェクト側の指示ファイルへ分離する。
- 2026-08-09: 【置き換え済み】共通指示の正本は `AGENTS.md` とし、Claude Code 用の `CLAUDE.md` は `@~/.codex/AGENTS.md` をインポートする方針だった。Codex がない端末で Claude Code を単独利用する場合に依存関係が残るため置き換えた。
- 2026-08-09: 共通指示の正本は `AGENTS.md` とする。`AGENTS.md` と `CLAUDE.md` は常に `~/.codex/` と `~/.claude/` の両方に配置する。Claude Code 用の `CLAUDE.md` は、同じディレクトリにある `AGENTS.md` を `@AGENTS.md` で相対インポートする。
- 2026-08-09: 【置き換え済み】AI 開発で混同しやすいツール固有のファイル名・パス・コマンドは、指示ファイル本体には入れず、`misc/ai-dev-quick-reference.html` に最終確認日と一次情報リンク付きで維持する方針だった。GitHub Pagesのブランチ公開元として扱いやすい `docs/` へ移行した。
- 2026-08-09: 【置き換え済み】`misc/` は GitHub Pages で公開する個人用AI開発リファレンスとする方針だった。GitHub Pagesのブランチ公開元として扱いやすい `docs/` へ移行した。
- 2026-08-09: AI 開発で混同しやすいツール固有のファイル名・パス・コマンドは、指示ファイル本体には入れず、`docs/ai-dev-quick-reference.html` に最終確認日と一次情報リンク付きで維持する。`docs/` は GitHub Pages で公開する個人用AI開発リファレンスとし、`index.html` を入口にする。
