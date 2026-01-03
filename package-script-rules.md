# パッケージスクリプト実行ルール

Node.js プロジェクトでスクリプトを実行する際のルール

## 基本方針

- スクリプト実行前に必ず `package.json` を読み、利用可能なスクリプトを確認する
- パッケージマネージャーのコマンドは `@antfu/ni` を使用する

## @antfu/ni について

> npm i in a yarn project, again? F**k!

プロジェクトごとに異なるパッケージマネージャー (npm/yarn/pnpm/bun) を自動判別して適切なコマンドを実行する。

## コマンド対応表

- `ni` - パッケージのインストール (`npm install` / `yarn` / `pnpm install` 相当)
- `nr <script>` - スクリプトの実行 (`npm run` / `yarn run` / `pnpm run` 相当)
- `nu` - パッケージの更新
- `nun <package>` - パッケージのアンインストール
- `nci` - クリーンインストール (`npm ci` 相当)

## 実行手順

- `package.json` の `scripts` セクションを確認
- 目的のスクリプトが存在するか確認
- `nr <script>` で実行
