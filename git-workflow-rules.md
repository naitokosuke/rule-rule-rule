# Git ワークフロールール

作業とコミットに関するルール

## ブランチ運用

- issue ベースでブランチを作成する
- 命名形式: `<issue番号>-<機能名>` (例: `123-add-login-feature`)

## コミット

### 粒度

- 1 機能 1 コミットを基本とする
- WIP コミットは PR マージ時に squash する前提で許可

### メッセージ形式

- Conventional Commits 形式を使用
- 1 行で完結させる
- 英語で記述する

### type 一覧

- `feat` - 新機能
- `fix` - バグ修正
- `docs` - ドキュメントのみの変更
- `style` - コードの意味に影響しない変更 (空白、フォーマットなど)
- `refactor` - バグ修正でも機能追加でもないコード変更
- `perf` - パフォーマンス改善
- `test` - テストの追加・修正
- `chore` - ビルドプロセスやツールの変更

### 例

- `feat: add user authentication`
- `fix: resolve null pointer in login flow`
- `refactor: extract validation logic`

## コミット前の検証

- テストとリントが通ることを確認してからコミットする
- 検証コマンドの実行には `nr` を使用する (package.json の scripts を事前に確認)
