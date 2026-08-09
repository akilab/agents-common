# Decisions

- 2026-08-09: `AGENTS.md` / `CLAUDE.md` は、特定のプロジェクト・技術スタック・組織固有の運用に依存させず、端末変更時にもそのままコピーして使える汎用指示として設計する。個別事情は各プロジェクト側の指示ファイルへ分離する。
- 2026-08-09: 【置き換え済み】共通指示の正本は `AGENTS.md` とし、Claude Code 用の `CLAUDE.md` は `@~/.codex/AGENTS.md` をインポートする方針だった。Codex がない端末で Claude Code を単独利用する場合に依存関係が残るため置き換えた。
- 2026-08-09: 共通指示の正本は `AGENTS.md` とする。`AGENTS.md` と `CLAUDE.md` は常に `~/.codex/` と `~/.claude/` の両方に配置する。Claude Code 用の `CLAUDE.md` は、同じディレクトリにある `AGENTS.md` を `@AGENTS.md` で相対インポートする。
