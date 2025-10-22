---
layout: default
title: Home
---

# Hey, I'm Amir Mojiri 👋

I'm a web developer who enjoys building thoughtful interfaces, sharing product lessons, and keeping privacy promises front and center.

<p>
  <a class="btn" href="{{ '/apps/' | relative_url }}">Explore my apps</a>
  <a class="btn" href="{{ '/blog/' | relative_url }}">Read the blog</a>
</p>

## About

I focus on performant, accessible experiences across the web and mobile. This site serves as a hub for current projects, product notes, and transparent policies.

## Featured app

- **Sample App** — A placeholder project showing how each app page is structured.  
  [Intro page]({{ '/apps/sample-app/' | relative_url }}) • [Privacy policy]({{ '/apps/sample-app/privacy/' | relative_url }})

## Latest post

{% assign latest_post = site.posts | first %}
{% if latest_post %}

- **[{{ latest_post.title }}]({{ latest_post.url | relative_url }})**  
   <small>{{ latest_post.date | date: "%b %-d, %Y" }}</small>  
   {{ latest_post.excerpt | strip_html | truncate: 140 }}
  {% else %}
- Posts are on the way. Check back soon!
  {% endif %}

## Contact

- Email: [hello@amirMojiri.dev](mailto:hello@amirMojiri.dev)
- GitHub: [@amirMojiri](https://github.com/amirMojiri)
