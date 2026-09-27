# COMMAND — 開発コマンド

```sh
bundle install            # gem 導入 (初回)
bundle exec jekyll serve  # ローカル開発サーバ + ライブリロード
bundle exec jekyll build  # _site/ へビルド (jekyll b も可)

# jekyll-compose (正しい frontmatter 付きで記事雛形生成)
bundle exec jekyll post "タイトル"    # _posts/ に日付付き記事
bundle exec jekyll draft "タイトル"   # _drafts/ に下書き
```

テスト・lint なし。CI (`ruby/setup-ruby`, Ruby 3.1) は `JEKYLL_ENV=production` でビルド → `_site/` を Pages へデプロイ。
