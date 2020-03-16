---
layout: default.liquid
title: Blog
categories: [blog]
data:
  head-img: images/eggbox.jpg
---

<ol>
{% for post in collections.posts.pages %}
{% if post.is_draft == false %}
<li>
{{ post.published_date | date: "%d %B %Y" }} — <a href="{{ post.permalink }}">{{ post.title }}</a>
</li>
{% endif %}
{% endfor %}
</ol>
