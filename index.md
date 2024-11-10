---
layout: default
title: "Welcome to My Portfolio"
permalink: /
---

# Welcome to my portfolio!
Explore my collection of paintings, photography, and AI-generated art.

{% for post in site.posts limit:5 %}
  <h2>{{ post.title }}</h2>
  <p>{{ post.excerpt }}</p>
  <a href="{{ post.url | relative_url }}">Read more</a>
  <hr>
{% endfor %}


