---
layout: post
permalink: /blog
headline: Blog - Aarti Menghani
title: 'Blog - Aarti Menghani'
bClass: blog
---

<section class="blog">
    {% if site.paginate %}
    {% assign posts = paginator.posts %}
    {% else %}
    {% assign posts = site.posts %}
    {% endif %}


    {%- if posts.size > 0 -%}
    {%- if page.list_title -%}
    <h2 class="post-list-heading">{{ page.list_title }}</h2>
    {%- endif -%}
    <div class="post-list">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        {%- for post in posts -%}
        <div class='post__outer'>
            <span class="post-meta"><i class="fa fa-calendar"></i> {{ post.date | date: date_format }}</span>
            <h3 class="post__title">
                <a class="post-link" href="{{ post.url | relative_url }}">
                    {{ post.title | escape }}
                </a>
            </h3>
            <p class="article__excerpt">
                {% if post.description %}{{ post.description }}{% else %}{{ post.content | strip_html | truncate: 185 }}{% endif %}
            </p>

            <a href="{{ post.url | relative_url }}" class="read-more">Keep Reading <i
                    class="fa fa-long-arrow-right"></i></a>
        </div>
        {%- endfor -%}
    </div>

    {% if site.paginate %}
    <div class="pager">
        <ul class="pagination">
            {%- if paginator.previous_page %}
            <li><a href="{{ paginator.previous_page_path | relative_url }}"
                    class="previous-page">{{ paginator.previous_page }}</a></li>
            {%- else %}
            <li>
                <div class="pager-edge">•</div>
            </li>
            {%- endif %}
            <li>
                <div class="current-page">{{ paginator.page }}</div>
            </li>
            {%- if paginator.next_page %}
            <li><a href="{{ paginator.next_page_path | relative_url }}" class="next-page">{{ paginator.next_page }}</a>
            </li>
            {%- else %}
            <li>
                <div class="pager-edge">•</div>
            </li>
            {%- endif %}
        </ul>
    </div>
    {%- endif %}

    {%- endif -%}
</section>