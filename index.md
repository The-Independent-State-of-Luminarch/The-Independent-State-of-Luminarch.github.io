---
layout: default
title: ホーム
---

# Luminarch独立国へようこそ
## 最新情報

- [開発者ブログ](/developer-blog/) ← 修正
- [歴史](/history/)

## お知らせ

準備中...

## 最近の開発ブログ

{% assign recent_dev_posts = site.posts | where: "categories", "developer-blog" | limit: 3 %}
{% for post in recent_dev_posts %}
- **{{ post.date | date: "%m/%d" }}** [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% if recent_dev_posts.size == 0 %}
まだ記事がありません。
{% endif %}

[すべての記事を見る →](/developer-blog/)
