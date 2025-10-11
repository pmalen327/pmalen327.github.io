---
layout: default
title: Journal
permalink: /journal/
nav: journal
---

# Journal

Mathematical notes, sketches, and thoughts. Newest first. Use LaTeX like $\\int_0^1 x^2 \\, dx$ or display:

$$
\\nabla \\cdot (\\nabla u) = 0
$$

## Archive by Month

{% assign sorted = site.posts | sort: "date" | reverse %}
{% assign grouped = sorted | group_by_exp: "post", "post.date | date: '%B %Y'" %}

{% for month in grouped %}
<div class="archive-month" id="{{ month.name | downcase | replace: ' ', '-' }}">
  {{ month.name }}
</div>
<ul class="post-list">
  {% for post in month.items %}
  <li>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <div class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</div>
    {% if post.excerpt %}{{ post.excerpt | strip_html | truncate: 160 }}{% endif %}
  </li>
  {% endfor %}
</ul>
{% endfor %}
