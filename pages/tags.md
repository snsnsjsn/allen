---
layout: default
title: 标签
permalink: /pages/tags.html
---

# 标签

{% for tag in site.tags %}
## #{{ tag[0] }}

{% for post in tag[1] %}
- [{{ post.title }}]({{ post.url | relative_url }}) · {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% endfor %}
