# 運転免許試験問題練習サイト

運転免許試験の練習問題を解くことができるWebアプリケーションです。

## 機能

- 6つの問題集（集検1～6）から選択可能
- 練習モード（即座に正解表示）と試験モード（最後に結果表示）
- 間違えた問題の再挑戦機能
- 完璧なスコア時の自動TOP画面復帰

## ファイル構造

```
├── index.html              # メインのHTMLファイル
├── assets/
│   ├── data/               # JSON問題ファイル
│   │   ├── 1.json
│   │   ├── 2.json
│   │   ├── 3.json
│   │   ├── 4.json
│   │   ├── 5.json
│   │   └── 6.json
│   └── images/             # 問題画像ファイル
│       ├── 1-1.png
│       ├── 1-2.png
│       └── ...
└── .github/workflows/      # GitHub Pagesデプロイ設定
    └── deploy.yml
```

## ローカルでの実行

1. ローカルサーバーを起動：
   ```bash
   # Python 3の場合
   python -m http.server 8000
   
   # Node.jsの場合
   npx http-server
   ```

2. ブラウザで `http://localhost:8000` にアクセス

## GitHub Pagesでのデプロイ

### 自動デプロイ（推奨）

1. このリポジトリをGitHubにプッシュ
2. リポジトリの設定で「Pages」を有効化
3. ソースを「GitHub Actions」に設定
4. `main`ブランチにプッシュすると自動的にデプロイされます

### 手動デプロイ

1. リポジトリの設定で「Pages」を有効化
2. ソースを「Deploy from a branch」に設定
3. ブランチを`main`に設定
4. フォルダを`/ (root)`に設定

## 問題データの更新

JSONファイルを編集した場合：

1. `assets/data/`フォルダ内の対応するJSONファイルを編集
2. 変更をコミットしてプッシュ
3. GitHub Pagesが自動的に更新されます

## 技術仕様

- HTML5 + CSS3 + JavaScript (ES6+)
- レスポンシブデザイン対応
- モダンブラウザ対応（Chrome, Firefox, Safari, Edge）

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。 