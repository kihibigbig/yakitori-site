# 焼鳥 友（仮） - GitHub Pages 公開手順

このリポジトリは、焼き鳥屋さんのシンプルな静的サイトです。以下の手順で GitHub に公開できます。

1. GitHub 側で新しいリポジトリを作成（例: `yakitori-tomo`）
2. ローカルでリポジトリを初期化してコミット

Windows の `cmd.exe` でのサンプルコマンド:

```bash
cd "C:\Users\kihib\OneDrive\デスクトップ\焼き鳥\ホームページ"
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<あなたのユーザー名>/<リポジトリ名>.git
git push -u origin main
```

3. GitHub のリポジトリ設定 > Pages に移動し、公開ソースを `main` ブランチの `/ (root)` に設定して保存します。

4. 反映されるまで数分待つと `https://<あなたのユーザー名>.github.io/<リポジトリ名>/` でサイトが表示されます。

ローカルで確認する方法:

- 簡易サーバ（Python がある場合）:
```bash
python -m http.server 8000
# ブラウザで http://localhost:8000 を開く
```

カスタマイズのポイント:
- お店の名前、住所、電話番号、営業時間を `index.html` 内で書き換えてください。
- 画像を入れる場合は `assets/` フォルダを作り、`<img>` タグで参照してください。
- カスタムドメインを使う場合は `CNAME` ファイルを追加してください。
- メニューの更新は `index.html` の `<section id="menu">` 以下を編集してください。カテゴリーごとに `<article class="menu-section">` を複製すると追加が簡単です。

問題があれば手伝います。公開後にURLを教えてください。サポートします。
