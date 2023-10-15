---
layout: default
title: Poem
permalink: /poems
---

<section class="poem">
    {% for poem in site.poems %}
    <h2><a href="{{ poem.url }}">{{ poem.title }}</a></h2>
    <p>{{ poem.content | markdownify }}</p>
    {% endfor %}
</section>