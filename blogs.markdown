---
layout: default
title: Blog
---

<div class="blog-list">
  {% for post in site.blogs %}
    <article>
        <h2><a class="title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt }}</p>
        <a href="{{ post.url | relative_url }}">Read More</a>
    </article>
  {% endfor %}
</div>
