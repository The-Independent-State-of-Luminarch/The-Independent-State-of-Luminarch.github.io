---
layout: default
title: ホーム
---

## 新着記事
<ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }} — {{ post.title }}</a></li>
{% endfor %}
</ul>
