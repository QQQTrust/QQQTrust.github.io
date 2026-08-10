---
layout: default
title: 归档
permalink: /archive/
---

<main class="simple-page">
  <h1>归档</h1>
  <div class="archive-list">
    {% assign ordered_posts = site.posts | sort: "order" %}
    {% for post in ordered_posts %}
      {% if post.reddit_id %}
        <a class="archive-item" href="{{ post.url | relative_url }}">
          <time>{{ post.date | date: '%Y-%m-%d' }}</time>
          <span>{{ post.title }}</span>
        </a>
      {% endif %}
    {% endfor %}
  </div>
</main>
