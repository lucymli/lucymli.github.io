---
layout: page
title: Blog Posts
permalink: /posts/
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}/posts">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>