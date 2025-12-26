---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Browse all posts below (newest first).

<ul>
  {% assign posts_sorted = site.posts %}
  {% for post in posts_sorted %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small> — {{ post.date | date: "%b %d, %Y" }}</small>
      {% if post.categories and post.categories.size > 0 %}
        <small> • {{ post.categories | join: ", " }}</small>
      {% endif %}
    </li>
  {% endfor %}
</ul>
