# Cloudflare-Sample
Cloudflare調査・検証用のリポジトリです。

## Cloudflareとは

Cloudflare（クラウドフレア）とは、CDNなどを提供するサービスのこと。

CDNを提供するサービスは複数ありますが、世界シェア1位を誇っているのがCloudflare。

## Cloudflare Workers

Cloudflare Workersは**サーバーレス・エッジコンピューティングサービス**です。

## Cloudflareのメリット

- ページ表示の高速化ができる
- 設定が簡単にできる
- 無料でも導入できる
- セキュリティ対策強化ができる
- 信頼性の高いサイト構築ができる
- 画像変換や待機室など機能が充実

## Cloudflareのデメリット

- Cloudflareがダウンするとサイトの利用ができない
- WordPressを利用している場合は注意が必要
- 適切に運用するには知識が必要

## AWS LambdaやGCP Cloud Runとの比較
Cloudflare Workersと似たコンセプトのサービスとしてAWS LambdaやGoogle Cloudの Cloud Runがあります。

これらのサービスとの違いは、コンテナ仮想化を利用していない点です。

LambdaやCloud Runはコンテナ仮想化を利用しています。一方、JavaScriptランタイムのV8を実質的な仮想化ソフトウェアとして利用しているのがCloudflare Workersの特徴です。

**Cloudflare Workers** の場合はコンテナの起動を待つ必要がありません。

従って、コールドスタートとホットスタートの概念はありません。言うならばCloudflare Workersは常にホットな状態。

## テンプレートプロジェクトの開始方法

```bash
npm create cloudflare@latest my-first-worker
```

以下のように出力されればOK!

```bash
👋 Welcome to create-cloudflare v2.35.1!
🧡 Let's get started.
📊 Cloudflare collects telemetry about your usage of Create-Cloudflare.

Learn more at: https://github.com/cloudflare/workers-sdk/blob/main/packages/create-cloudflare/telemetry.md
───────────────────────────────────────────────────────────────────────────────────────────────────────

╭ Create an application with Cloudflare Step 1 of 3
│
├ In which directory do you want to create your application?
│ dir ./my-first-worker
│
├ What would you like to start with?
│ category Hello World example
│
├ Which template would you like to use?
│ type Hello World Worker
│
├ Which language do you want to use?
│ lang TypeScript
│
├ Copying template files
│ files copied to project directory
│
├ Updating name in `package.json`
│ updated `package.json`
│
├ Installing dependencies
│ installed via `npm install`
│
╰ Application created

╭ Configuring your application for Cloudflare Step 2 of 3
│
├ Installing @cloudflare/workers-types
│ installed via npm
│
├ Adding latest types to `tsconfig.json`
│ added @cloudflare/workers-types/2023-07-01
│
├ Retrieving current workerd compatibility date
│ compatibility date 2024-12-24
│
╰ Application configured 

╭ Deploy with Cloudflare Step 3 of 3
│
├ Do you want to deploy your application?
│ no deploy via `npm run deploy`
│
╰ Done 

────────────────────────────────────────────────────────────
🎉  SUCCESS  Application created successfully!

💻 Continue Developing
Change directories: cd my-first-worker
Start dev server: npm run start
Deploy: npm run deploy

📖 Explore Documentation
https://developers.cloudflare.com/workers

🐛 Report an Issue
https://github.com/cloudflare/workers-sdk/issues/new/choose

💬 Join our Community
https://discord.cloudflare.com
```

もしくは以下のコマンドで生成

```bash
wrangler generate projectname https://github.com/cloudflare/worker-template
```

## 動かし方

- 依存関係のインストール

    ```bash
    bun install
    ```

- テスト実行

    ```bash
    bun run dev
    ```

### 参考文献
1. [Cloudflare 公式サイト](https://www.cloudflare.com/ja-jp/learning/what-is-cloudflare/)
2. [Cloudflare（クラウドフレア）とは？仕組みや導入するメリット](https://www.accelia.net/column/beginners/6462/)
3. [Cloudflare workres 紹介ページ](https://developers.cloudflare.com/workers/)
4. [Cloudflare workres Get Started](https://developers.cloudflare.com/workers/get-started/guide/)
5. [Cloudflare workes チュートリアル](https://developers.cloudflare.com/workers/tutorials/)
6. [Cloudflare Workersのチュートリアルをやってみた](https://dev.classmethod.jp/articles/cloudflare-workers-tutorial/)
7. [Zenn - 入門Cloudflare Workers](https://zenn.dev/moutend/articles/97c98a277f4bae)