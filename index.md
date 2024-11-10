---
layout: default
title: "Welcome to My Portfolio"
permalink: /
---

# Welcome to my portfolio!
Explore my collection of paintings, photographies, and AI-generated art.

{% for post in site.posts limit:5 %}
  <h2>{{ post.title }}</h2>
  {% if post.image %}
    <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="max-width: 100%; height: auto;">
  {% endif %}
  <p>{{ post.excerpt }}</p>
  <a href="{{ post.url | relative_url }}">Read more</a>
  <hr>
{% endfor %}


