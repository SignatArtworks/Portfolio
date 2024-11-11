---
layout: default
title: "Simon Ignat"
permalink: /
---

Explore my collection of paintings, photographies, and AI-generated art.

# Oil and Acrylic Paintings

{% assign random_seed = site.time | date: "%s" | plus: 0 %} <!-- Use current timestamp as a seed -->
{% assign shuffled_posts = site.posts | sort: "date" | reverse %} <!-- Sort by date to standardize order -->
{% assign shuffled_posts = shuffled_posts | slice: 0, 10 %} <!-- Limit to 10 posts if needed -->

{% for post in shuffled_posts %}
  <h2>{{ post.title }}</h2>
  {% if post.image %}
    <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="max-width: 50%; height: auto;">
  {% endif %}
  <p>{{ post.excerpt }}</p>
  <a href="{{ post.url | relative_url }}">Read more</a>
  <hr>
{% endfor %}


