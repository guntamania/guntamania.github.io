# ARCHITECTURE — サイト構造

標準 Jekyll。ただし **`minima` テーマを独自レイアウトで上書き** — デフォルトの minima 挙動を前提にしない。

## レイアウト継承

`home.html` / `archives.html` / `post.html` → すべて `base.html` を継承。`base.html` が `<head>` (jQuery, fittext.js, script.js, Google Fonts Jost, GA gtag, `{% seo %}`) と `footer.html` を保持。

## ページ

- `index.markdown` は `layout: home`。トップは **時系列フィードではない** — `home.html` が Liquid で category 別に振り分け:
  - `categories: blog` → 最新3件を `_includes/blog_block.html` で描画、残りは `archives` へリンク。
  - `categories: product` → 全件を `_includes/product_block.html` で描画 (`image` と `tags` frontmatter 使用)。
- `archives.markdown` (`layout: archives`) は全記事を `_includes/post_list.html` で一覧。
- `about.markdown` — プロフィール。`404.html` — エラーページ。

## インクルード (`_includes/`)

- `blog_block.html` — ブログ記事カード (日付・タイトル・抜粋)。
- `product_block.html` — 制作物カード (スクショ・説明・タグ)。
- `post_list.html` — アーカイブ用一覧。
- `footer.html` — フッター。

## 補足

- `_site/` は生成物 (gitignore 済み) — 手編集しない。
- スタイル: `assets/css/style.scss` 1本 (Sass → `style.css`)。
- `.roo/mcp.json` は Roo/MCP ツール設定。サイト内容ではない。
