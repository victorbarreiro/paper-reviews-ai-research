---
layout: page
title: Teaching Materials
permalink: /teaching/
---

# Teaching and disemination Materials

{% assign teaching_posts = site.posts | where: "category", "teaching" %}
{% for post in teaching_posts %}
  <article class="post-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    <a href="{{ post.url | relative_url }}" class="read-more">Read tutorial →</a>
  </article>
{% endfor %}

