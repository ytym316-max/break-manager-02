# Break Manager

休憩時間管理アプリ。

## Vercelへのデプロイ手順

### 1. GitHubにアップロード

1. [github.com](https://github.com) でアカウント作成（または既存のアカウントでログイン）
2. 「New repository」でリポジトリを作成（名前は `break-manager` など）
3. このフォルダの中身を全部アップロード

**コマンドラインの場合：**
```bash
cd break-manager
git init
git add .
git commit -m "initial"
git remote add origin https://github.com/あなたのユーザー名/break-manager.git
git push -u origin main
```

### 2. Vercelでデプロイ

1. [vercel.com](https://vercel.com) でGitHubアカウントでログイン
2. 「Add New Project」→ 作ったリポジトリを選択
3. 設定はそのままで「Deploy」ボタンを押すだけ

数分で `https://break-manager-xxx.vercel.app` のようなURLが発行されます。

### スマホのホーム画面に追加（PWA風）

- **iPhone**: Safariで開いて「共有」→「ホーム画面に追加」
- **Android**: Chromeで開いて「メニュー」→「ホーム画面に追加」

## ローカルで動かす場合

```bash
npm install
npm run dev
```

## 仕様

- 休憩タイマー（カウントアップ）
- 17:15以降の休憩は×1.25換算
- 1日の目標：38分45秒（7時間45分 × 5分/時間）
- バックグラウンドでも開始時刻ベースで正確にカウント
- データはブラウザのlocalStorageに保存
- カレンダーで過去の記録を確認可能
