---
layout: default
title: "Simon Ignat"
permalink: /
---

# Oil and Acrylic Paintings

{% assign random_seed = site.time | date: "%s" | plus: 0 %}
{% assign shuffled_posts = site.posts | sort: "date" | reverse %}

{% for post in shuffled_posts %}
<h2>{{ post.title }}</h2>
{% if post.image %}
<img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="max-width: 50%; height: auto;">
{% endif %}
<p>{{ post.excerpt }}</p>
<a href="{{ post.url | relative_url }}">Read more</a>
<hr>
{% endfor %}

