---
layout: default
title: Index test page
---

@mizti $B$N%a%bMQ%Z!<%8$G$9!#(Bgithub pages$B$O?t<0$,=q$-$d$9$$$N$G<0B?$a$N%(%s%H%j$O$3$A$i$G!#$=$NB>$O(B http://mizti.hatenablog.com $B$K$F!#(B

<ul>
{% for post in site.posts %}
  <li>&raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
