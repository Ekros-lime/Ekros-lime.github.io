---
layout: default
title: Home
---

# Welcome to my Blogs!

{% assign years = site.posts | map: "date" | map: "year" | uniq | sort | reverse %}

<div style="margin-bottom: 20px;">
  <strong>ALL</strong>
  {% for y in years %}
    | <a href="#year-{{ y }}">{{ y }}</a>
  {% endfor %}
</div>

{% for y in years %}
### <a id="year-{{ y }}"></a>{{ y }}

{% assign posts_in_year = site.posts | where_exp: "post", "post.date | date: '%Y' == '#{y}'" %}

{% for post in posts_in_year %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url }})
{% endfor %}

---
{% endfor %}
