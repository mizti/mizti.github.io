---
layout: default
title: Index test page
---
{{ site }}
{% for post in site.posts %}
  <li>&raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
