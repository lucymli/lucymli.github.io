---
layout: page
show_meta: false
title: "Projects"
subheadline: ""
permalink: "/projects/"
---
<ul>
    {% for post in site.categories.design %}
    <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>