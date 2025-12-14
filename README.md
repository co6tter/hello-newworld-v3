# hello-newworld-v3

レスポンシブ対応のシンプルな静的Webサイトです。「Practice makes perfect（練習することで完璧になる）」をテーマに、日々の練習を促進することを目的としています。

## Overview

このプロジェクトは、HTML/CSS/JavaScriptの基礎練習を目的とした静的Webサイトです。モダンなデザインとレスポンシブレイアウトを実装し、AWS S3とCloudFrontを使用したホスティングを行っています。

主な機能:
- レスポンシブデザイン（PC・タブレット・スマートフォン対応）
- ハンバーガーメニュー（モバイル表示時）
- スムーススクロール
- コンタクトフォーム
- サービス紹介カード

## Tech Stack

- **HTML5**: セマンティックなマークアップ
- **CSS3**: カスタムCSS変数、Flexbox、Grid、モダンなレイアウト
- **JavaScript**: Vanilla JS（ドロワーメニューの制御）
- **デプロイ**: GitHub Actions + AWS S3 + CloudFront

## Setup

ローカル環境でのセットアップ方法:

```bash
# リポジトリのクローン
git clone https://github.com/your-username/hello-newworld-v3.git

# プロジェクトディレクトリに移動
cd hello-newworld-v3

# ローカルサーバーで起動（例: Live Serverなど）
# または、index.htmlをブラウザで直接開く
```

## Usage

### ローカル開発

任意のHTTPサーバーを使用してローカルで実行できます:

```bash
# Python3の場合
python3 -m http.server 8000

# Node.jsのhttp-serverを使用する場合
npx http-server
```

その後、ブラウザで `http://localhost:8000` を開きます。

### デプロイ

mainブランチにプッシュすると、GitHub Actionsが自動的にAWS S3とCloudFrontにデプロイします。

デプロイに必要なGitHub Secretsの設定:
- `S3_BUCKET`: S3バケット名
- `CF_DIST_ID`: CloudFrontディストリビューションID
- `REGION`: AWSリージョン
- `ROLE_ARN`: IAMロールARN

## Directory Structure

```
hello-newworld-v3/
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actionsデプロイ設定
├── css/
│   └── style.css          # メインスタイルシート
├── js/
│   └── script.js          # JavaScriptファイル
├── index.html             # メインページ
├── error.html             # エラーページ
└── README.md              # このファイル
```

## License

This repository is for personal/private use only.
