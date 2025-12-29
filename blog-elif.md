---
layout: default
title: Explain Like I'm Five (ELIF)
permalink: /blog/elif/
---

# Explain Like I'm Five (ELIF)

Posts where I break down technical concepts I work with in plain language.

<ul>
  {% for post in site.categories.elif %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small> — {{ post.date | date: "%b %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
