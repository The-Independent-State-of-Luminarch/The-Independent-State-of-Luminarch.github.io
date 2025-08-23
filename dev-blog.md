---
layout: default
title: 開発者ブログ
permalink: /dev-blog/
---

# 開発者ブログ

技術実装記録、学習メモ、開発tips などを投稿しています。

{% assign dev_posts = site.posts | where: "categories", "dev-blog" %}

{% for post in dev_posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

**{{ post.date | date: "%Y年%m月%d日" }}**

{% if post.tags.size > 0 %}
{% for tag in post.tags %}
<span style="background: var(--nav-hover); padding: 0.2rem 0.5rem; border-radius: 3px; font-size: 0.8rem; margin-right: 0.5rem;">#{{ tag }}</span>
{% endfor %}
{% endif %}

{{ post.excerpt }}

[続きを読む]({{ post.url | relative_url }})

---
{% endfor %}

{% if dev_posts.size == 0 %}
## まだ記事がありません
