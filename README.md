# カレンダーアプリ（React + Vite）

スマホ向けカレンダー・タスク管理アプリです。Vercelにそのままデプロイできます。

## ローカルで動かす

```bash
npm install
npm run dev
```

## Vercelへデプロイする方法

### 方法A: Vercel CLIを使う
```bash
npm install -g vercel
vercel
```
あとは指示に従ってログイン・プロジェクト名を入力するだけです。

### 方法B: GitHub経由でデプロイ
1. このフォルダの中身をGitHubリポジトリにpushする
2. https://vercel.com にログインし「Add New > Project」からそのリポジトリを選択
3. Framework Preset は「Vite」が自動検出されます（vercel.jsonでも明示済み）
4. 「Deploy」をクリックすれば数十秒で公開されます

## データの保存について
予定・タスク・色の名前・テンプレート・履歴などは、ブラウザのlocalStorageに保存されます。
サーバー側にデータベースは持っていないため、端末・ブラウザを変えるとデータは引き継がれません。

## ファイル構成
```
calendar-app/
├── index.html          Viteのエントリーhtml
├── package.json
├── vite.config.js
├── vercel.json          Vercel向けビルド設定
└── src/
    ├── main.jsx         Reactのマウント処理
    ├── App.jsx           ルートコンポーネント
    ├── App.css           アプリのスタイル
    ├── index.css         ベースのリセットCSS
    └── calendarApp.js    カレンダー本体のロジック（DOM操作で描画）
```
