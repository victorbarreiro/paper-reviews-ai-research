---
layout: page
title: Resources
permalink: /resources/
---

A comprehensive collection of books, videos and websites to support your AI research in good way.

{% assign resource_posts = site.posts | where: "category", "resources" %}
{% for post in resource_posts %}
  <article class="post-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    <a href="{{ post.url | relative_url }}" class="read-more">View resources →</a>
  </article>
{% endfor %}

