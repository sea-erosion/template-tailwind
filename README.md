# Next.js Tailwind Template

Next.js (App Router) + React + TypeScript + Tailwind CSS の GitHub Codespaces 用テンプレート。ESLint / Prettier 設定済み。

## 使い方

1. このリポジトリで **Code → Codespaces → Create codespace on main** を選択
2. コンテナ作成後、`postCreateCommand` で自動的に `npm install` が実行される
3. ターミナルで開発サーバーを起動

   ```bash
   npm run dev
   ```

4. ポート 3000 が自動でフォワードされ、プレビューが開く

## スクリプト

| コマンド               | 内容                                |
| ---------------------- | ----------------------------------- |
| `npm run dev`          | 開発サーバー起動                    |
| `npm run build`        | 本番ビルド                          |
| `npm run start`        | 本番サーバー起動                    |
| `npm run lint`         | ESLint チェック                     |
| `npm run lint:fix`     | ESLint 自動修正                     |
| `npm run format`       | Prettier で全ファイル整形           |
| `npm run format:check` | Prettier 整形チェックのみ（CI向け） |
| `npm run typecheck`    | TypeScript の型チェックのみ実行     |

## 構成

- **Next.js 15**（App Router）/ **React 19** / **TypeScript**
- **Tailwind CSS v4**（`app/globals.css` に `@import "tailwindcss"` を記述するCSSファースト方式。`tailwind.config.js` は不要）
- **ESLint 9**（Flat Config, `eslint.config.mjs`）+ `eslint-config-next` + `eslint-config-prettier`（フォーマット関連ルールの衝突を回避）
- **Prettier**（`prettier-plugin-tailwindcss` でクラス名を自動整列）
- **.devcontainer**: VS Code拡張（ESLint / Prettier / Tailwind IntelliSense等）を自動インストールし、保存時フォーマット・保存時ESLint自動修正を有効化済み

## Tailwind CSS v4 について

v3までと異なり `tailwind.config.ts` の作成は必須ではありません。カスタムテーマ拡張が必要な場合は `app/globals.css` 内で `@theme` ディレクティブを使うか、必要に応じて `tailwind.config.ts` を追加してください。

## カスタマイズ

- ESLintのルール調整: `eslint.config.mjs`
- Prettierのスタイル調整: `.prettierrc.json`
- devcontainerに追加したいVS Code拡張・Featuresがあれば `.devcontainer/devcontainer.json` を編集
