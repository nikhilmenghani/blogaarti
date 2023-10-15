---
layout: blog
title: Blog
---

<section class="blog">
{% for post in site.blogs %}
  <article>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
      <a class="read-more-btn" href="{{ post.url | relative_url }}">Read More</a>
  </article>
{% endfor %}
</section>
