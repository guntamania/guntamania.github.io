# WRITE_BLOG — 記事執筆

記事は `_posts/` に `YYYY-MM-DD-slug.md` 形式。`categories` frontmatter が配置先と描画 include を決める。

## ブログ記事

`categories: blog`。トップ (最新3件) + アーカイブに表示。

```yaml
---
layout: post
title:  記事タイトル
date:  2025-08-21 23:30:00 +0900
categories: blog
---
```

## 制作物 (Works)

`categories: product` + `image:` (`/assets/image/` 配下パス) + `tags:` (カンマ区切り、技術ラベルとしてそのまま表示)。"Works" セクションに表示。

```yaml
---
layout: post
title:  "精算ちゃん"
categories: product
tags: Flutter, Firebase
image: /assets/image/screen-seisan.png
---
```

## 補足

- 記事画像は `assets/image/` に置き `/assets/image/<file>` で参照。
- `_config.yml` に `future: true` → 未来日付の記事もビルドされる。
