---
layout: page
title: Laura Bledaite
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="page-header">
  <h1>Latest posts</h1>
</div>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>