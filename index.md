---
layout: default
title: Index test page
---

@mizti のメモ用ページです。github pagesは数式が書きやすいので式多めのエントリはこちらで。その他は http://mizti.hatenablog.com にて。

<ul>
{% for post in site.posts %}
  <li>&raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
