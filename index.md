---
layout: default
title: Home
---

# Welcome to my Blogs!

{%- assign posts_by_year = site.posts
  | group_by_exp: "post", "post.date | date: '%Y'"
  | sort: "name"
  | reverse
-%}

<div style="margin-bottom: 20px;">
  <strong>ALL</strong>
  {%- for year in posts_by_year -%}
    | <a href="#year-{{ year.name }}">{{ year.name }}</a>
  {%- endfor -%}
</div>

{%- for year in posts_by_year -%}
### <a id="year-{{ year.name }}"></a>{{ year.name }}

{%- for post in year.items -%}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{%- endfor -%}

---
{%- endfor -%}
