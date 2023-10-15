---
layout: default
title: Home
---

<div class="ui stackable grid">
    <div class="twelve wide centered column">
        <main>
            {% for post in site.posts limit:5 %}
            <article class="ui segment">
                <h2 class="ui header"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
                <p>{{ post.excerpt }}</p>
                <a href="{{ post.url | relative_url }}" class="ui button blue">Read More</a>
            </article>
            {% endfor %}
        </main>
    </div>
</div>
