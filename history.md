---
layout: default
title: History
permalink: /history/
---

# History of Luminarch
you can learn about the history of the Luminarch.
## Timeline
### Operation Transcendence 
September 8, 2025 - The refurbished Tesla P40 purchased was cancelled by the seller 12 days later, resulting in the collapse of the quality component procurement plan at fair prices and confirmed time loss due to parts re-acquisition. Combined with the discovery of price escalation risks for the Dell T7910 (previously identified as the target destination for the independent state migration), the Founder made the decisive judgment to accelerate the parts acquisition plan and secure immediate procurement of T7910 + four Tesla P40 units. Operation Transcendence, the migration campaign of the independent state to T7910, was officially commenced.

September 10, 2025 - Successfully procured T7910 components. Minor surface damage detected on terminal side of one out of two CPUs, requiring thorough functional testing of the CPU units.

{% assign history_posts = site.posts | where: "categories", "history" %}
{% if history_posts.size > 0 %}

## Posts

{% for post in history_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% endif %}
