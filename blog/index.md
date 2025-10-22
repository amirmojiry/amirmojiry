---
layout: default
title: Blog
permalink: /blog/
---

Updates on projects, lessons learned while shipping apps, and personal notes from the journey.

{% if site.posts and site.posts != empty %}
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p><small>{{ post.date | date: "%b %-d, %Y" }}</small></p>
    <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
  </li>
  {% endfor %}
</ul>
{% else %}
<p>Posts are on the way. Stay tuned!</p>
{% endif %}
