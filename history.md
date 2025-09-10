---
layout: default
title: History
permalink: /history/
---

# History of Luminarch

coming soon

{% assign history_posts = site.posts | where: "categories", "history" %}
{% if history_posts.size > 0 %}

## Posts

{% for post in history_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% endif %}
