---
layout: default
title: 首页
---

<section class="hero">
  <h1>Allen.ee</h1>
  <p>技术分享、生活记录、项目进度与长期思考。</p>
</section>

<h2>最新文章</h2>

<div class="post-list">
{% for post in site.posts %}
  <article class="post-card">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="meta">{{ post.date | date: "%Y-%m-%d" }} · {{ post.categories | join: " / " }}</p>
    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    <p>
      {% for tag in post.tags %}
        <span class="tag">#{{ tag }}</span>
      {% endfor %}
    </p>
  </article>
{% endfor %}
</div>
