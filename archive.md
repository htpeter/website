---
layout: default
title: Archive
---

# Archive

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-date">{{ post.date | date: "%B %-d, %Y" }}</p>
  </li>
{% endfor %}
</ul>
