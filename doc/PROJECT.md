# PROJECT — guntamania.com

モバイルエンジニア guntama (Hiroki YAMADA) の個人サイト。ポートフォリオ + ブログ。

## 技術スタック

- Jekyll (静的サイトジェネレータ)
- テーマ: `minima` gem を導入するも、実体は独自レイアウトで上書き
- プラグイン: `jekyll-feed`, `jekyll-seo-tag`, `jekyll-compose`
- ホスティング: GitHub Pages
- ドメイン: guntamania.com (CNAME)
- アクセス解析: Google Analytics (gtag)

## デプロイ

`main` に push → GitHub Actions (`.github/workflows/jekyll.yml`) が Ruby 3.1 で `JEKYLL_ENV=production` ビルド → `_site/` を Pages へ公開。手動実行 (`workflow_dispatch`) も可。

## 掲載テーマ

Android / Kotlin / Ruby on Rails / Flutter / JavaScript / Vue.js / 暗号資産。

## 関連ドキュメント

- @COMMAND.md — 開発コマンド
- @ARCHITECTURE.md — サイト構造
- @WRITE_BLOG.md — 記事執筆
