# Make it easy - GitHub Pagesデモ

学生マッチングプラットフォーム「Make it easy」のデモアプリケーションです。

## 🚀 GitHub Pagesへのデプロイ方法

### 方法1: GitHubウェブUI経由（推奨・最も簡単）

1. **GitHubでリポジトリを作成**
   - GitHubにログインして「New repository」をクリック
   - リポジトリ名を入力（例: `make-it-easy-demo`）
   - Public/Privateを選択（Publicを推奨）
   - 「Create repository」をクリック

2. **ファイルをアップロード**
   - リポジトリページで「uploading an existing file」をクリック
   - 以下のファイルをドラッグ&ドロップ:
     - `index.html`
     - `.nojekyll`
     - `README.md`
   - 「Commit changes」をクリック

3. **GitHub Pagesを有効化**
   - リポジトリの「Settings」タブをクリック
   - 左サイドバーの「Pages」をクリック
   - 「Source」で「main」ブランチを選択
   - 「Save」をクリック

4. **公開URLを確認**
   - 数分後、同じページに公開URLが表示されます:
     ```
     https://[あなたのユーザー名].github.io/[リポジトリ名]/
     ```

### 方法2: Git CLI経由

```bash
# リポジトリを初期化
cd make-it-easy-github-pages
git init

# ファイルをステージング
git add .

# コミット
git commit -m "Initial commit: Make it easy demo"

# GitHubリポジトリを作成後、リモートを追加
git remote add origin https://github.com/[ユーザー名]/[リポジトリ名].git

# プッシュ
git branch -M main
git push -u origin main
```

その後、GitHubのSettings > Pagesでmainブランチを有効化してください。

### 方法3: GitHub Desktop経由

1. GitHub Desktopを開く
2. 「File」→「Add Local Repository」
3. `make-it-easy-github-pages`フォルダを選択
4. 「Publish repository」をクリック
5. GitHubのSettings > Pagesでmainブランチを有効化

## 📱 機能一覧

### 1. ホームページ
- アプリの紹介
- 主要機能へのナビゲーション
- デモモードの説明

### 2. ユーザー登録
- 氏名、メール、大学名、学年の入力
- 興味・関心のタグ付け
- 学生証認証（写真または動画アップロード）

### 3. グループ一覧
- 活動中のグループを閲覧
- グループ名・説明で検索
- カテゴリー別表示

### 4. マッチング申請
- マッチングタイプの選択（勉強仲間、趣味仲間、プロジェクト仲間、起業仲間）
- 興味分野の入力
- 自己紹介

### 5. 管理画面
- 統計情報の表示
- 登録ユーザー一覧
- マッチング申請一覧
- データ管理機能（リセット、削除、エクスポート）

## 🎨 デザイン

- **カラーテーマ**: エメラルドグリーン (#10B981)
- **最適化**: スマートフォン表示 (430×932px)
- **フレームワーク**: Tailwind CSS (CDN版)
- **レスポンシブ**: モバイルファーストデザイン

## 💾 データ保存

- **ストレージ**: ブラウザのLocalStorage
- **永続性**: ブラウザキャッシュをクリアするまで保持
- **サンプルデータ**: 初回アクセス時に自動投入

## 🔒 セキュリティ

このデモアプリは教育・デモンストレーション目的です。本番環境では以下を実装してください:

- バックエンドサーバー（Node.js + Express等）
- データベース（PostgreSQL、MongoDB等）
- 認証システム（JWT、OAuth等）
- HTTPS通信
- 入力バリデーション
- XSS/CSRF対策

## 📝 カスタマイズ

### カラーテーマの変更

`index.html`内のTailwindクラスを編集:

```html
<!-- 現在: エメラルドグリーン -->
<nav class="bg-emerald-500">

<!-- 他の色に変更（例: ブルー） -->
<nav class="bg-blue-500">
```

### サンプルデータの編集

`index.html`内の`initializeSampleData()`関数を編集してください。

## 🌐 公開後の確認事項

✅ すべてのページが正しく表示される  
✅ ナビゲーションが動作する  
✅ フォーム送信が機能する  
✅ データが保存される（LocalStorage）  
✅ 管理画面で統計が表示される  

## 🆘 トラブルシューティング

### ページが404エラーになる
- GitHub Pagesの設定でmainブランチが選択されているか確認
- ファイル名が`index.html`（小文字）であることを確認
- 数分待ってからアクセス（デプロイに時間がかかる場合があります）

### スタイルが適用されない
- ブラウザのキャッシュをクリア
- Tailwind CDNが読み込まれているか確認（開発者ツール → Network）

### データが保存されない
- LocalStorageが有効か確認（プライベートブラウジングモードでは無効）
- ブラウザの開発者ツール → Application → Local Storage を確認

## 📄 ライセンス

このデモアプリはMITライセンスの下で公開されています。

## 🤝 サポート

質問や問題がある場合は、GitHubのIssuesセクションでお知らせください。

---

**Make it easy** - 学生同士をつなぐマッチングプラットフォーム
