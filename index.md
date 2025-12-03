---
layout: default
title: Home
---

# Welcome to my Blogs!

{% for post in site.posts %}
* ### [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
