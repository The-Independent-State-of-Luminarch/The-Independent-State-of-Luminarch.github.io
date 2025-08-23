---
layout: default
title: ホーム
---

# Welcome to Luminarch
## お知らせ

{% assign news_posts = site.posts | where_exp: "post", "post.categories.size == 0" | limit: 5 %}
{% for post in news_posts %}
- **{{ post.date | date: "%m/%d" }}** [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% if news_posts.size == 0 %}
現在お知らせはありません。
{% endif %}

## 最近の開発ブログ

{% assign recent_dev_posts = site.posts | where: "categories", "developer-blog" | limit: 3 %}
{% for post in recent_dev_posts %}
- **{{ post.date | date: "%m/%d" }}** [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% if recent_dev_posts.size == 0 %}
まだ開発ブログ記事がありません。
{% endif %}

[開発者ブログをすべて見る →](/developer-blog/)
