---
layout: default
title: 归档
permalink: /archive/
---

<main class="simple-page">
  <h1>归档</h1>
  <div class="archive-list">
    {% for post in site.posts %}
      <a class="archive-item" href="{{ post.url | relative_url }}">
        <time>{{ post.date | date: '%Y-%m-%d' }}</time>
        <span>{{ post.title }}</span>
      </a>
    {% endfor %}
  </div>
</main>
