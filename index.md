---
layout: page
title: Dy3RAwgoLD
tagline: 皆素
---
{% include JB/setup %}

## Latest posts

-----

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
    

----

### Not by me, but you can do this
Built based on [Jekyll Quickstart](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)
Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)
This theme is still unfinished. If you'd like to be added as a contributor, [please fork them](http://github.com/plusjade/jekyll-bootstrap).


