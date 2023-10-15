---
layout: default
title: Aarti's Portfolio
---

<div class="portfolio-container">
    <h1>Welcome to My Portfolio</h1>
    <p>Hello! I'm Aarti. This is a showcase of my work, projects, and achievements.</p>
    
    <section class="portfolio-items">
        {% for item in site.data.portfolio %}
        <div class="portfolio-item">
            <!-- <img src="{{ item.image }}" alt="{{ item.title }}"> -->
            <h2>{{ item.title }}</h2>
            <p>{{ item.description }}</p>
        </div>
        {% endfor %}
    </section>
</div>
