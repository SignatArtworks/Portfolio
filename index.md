---
layout: default
title: "Simon Ignat"
permalink: /
---

Explore my collection of paintings, photographies, and AI-generated art.

# Oil and Acrylic Paintings

{% for post in site.posts %}
<h2>{{ post.title }}</h2>
{% if post.image %}
<img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="max-width: 50%; height: auto;">
{% endif %}
<p>{{ post.excerpt }}</p>
<a href="{{ post.url | relative_url }}">Read more</a>
<hr>
{% endfor %}


