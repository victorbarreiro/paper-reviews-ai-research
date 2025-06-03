---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
permalink: /
---

# Welcome to Paper reivies and Research in AI

Hey everyone! I started this blog to share what I'm discovering in my  research and hopefully make some of the more complex stuff easier to digest. Since I'm constantly diving into literature reviews anyway (they're just part of the research game), I figured why not share some of the cool insights I stumble across along the way?

Sure, the main findings usually end up in published papers, but there's always  interesting knowledge that never makes it into those publications – either because it doesn't quite fit the specific focus of a study or just gets left on the cutting room floor. That's the stuff I want to talk about here!

{% assign paper_posts = site.posts | where: "category", "papers" %}
{% for post in paper_posts %}
  <article class="post-preview">
    {% if post.image %}
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }} image" class="post-image">
    {% endif %}
    <div class="post-content">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
      <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
    </div>
  </article>
{% endfor %}
