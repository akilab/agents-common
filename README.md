# agents-common

Codex と Claude Code で共通利用する、プロジェクトに依存しない指示ファイルのテンプレートです。

## 含まれるもの

- `AGENTS.md`: 共通指示の正本。作業メモ、指示の適用順、変更と検証の基本ルールを定めます。
- `CLAUDE.md`: `AGENTS.md` を読み込む Claude Code 用の薄いエントリポイントです。
- `working-memory/`: このテンプレートを整備する際の判断・作業記録です。実運用では、各プロジェクトの継続作業に必要な非機密情報を記録します。
- `docs/`: GitHub Pagesで公開するAI開発リファレンスです。Codex / Claude Code早見表、Codex CLI入門、Agents / Skills設計ガイドを含みます。

## 配置方法

新しい端末では、`AGENTS.md` と `CLAUDE.md` を両方の設定ディレクトリへ配置します。

```text
~/.codex/
├── AGENTS.md
└── CLAUDE.md

~/.claude/
├── AGENTS.md
└── CLAUDE.md
```

`CLAUDE.md` は同じディレクトリの `AGENTS.md` を `@AGENTS.md` で相対参照します。そのため、Codex がない端末で Claude Code だけを使う場合も動作します。

## 方針

- 共通指示には、どのプロジェクトでも有効な短いルールだけを置く。
- 技術スタック、ビルド方法、テスト手順などのプロジェクト固有ルールは、各リポジトリ側の指示ファイルへ分離する。
- 作業メモには秘密情報を保存しない。

## 早見表

ブラウザで [`docs/index.html`](docs/index.html) を開くと、早見表、Codex CLI入門、Agents / Skills 設計ガイドへ移動できます。GitHub Pagesでは `main` ブランチの `/docs` を公開元に指定してください。内容には最終確認日と公式ドキュメントへのリンクを付記しています。
