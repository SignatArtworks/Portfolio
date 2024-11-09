---
layout: default
title: "Welcome to My Portfolio"
permalink: /
---

# Welcome to my portfolio!
Explore my collection of paintings, photography, and AI-generated art.

## Recent Posts
{% for post in site.posts %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}

