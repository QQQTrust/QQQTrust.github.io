---
layout: default
title: 学习笔记
permalink: /learning-notes/
---

<main class="simple-page">
  <h1>学习笔记</h1>
  <p class="learning-intro">道氏理论系列，共 13 篇，按照 Reddit 原帖顺序排列。</p>

  <div class="learning-list">
    {% assign learning_posts = site.posts | where: "category", "学习笔记" | sort: "learning_order" %}
    {% for post in learning_posts %}
      <a class="learning-item" href="{{ post.url | relative_url }}">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%Y-%m-%d' }}</time>
        <h2>{{ post.title }}</h2>
        <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </a>
    {% endfor %}
  </div>
</main>
