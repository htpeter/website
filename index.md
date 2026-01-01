---
layout: default
title: Home
---

# {{ site.title }}

{{ site.description }}

## Recent Posts

<ul class="post-list">
{% for post in site.posts limit:10 %}
  <li>
    <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-date">{{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.excerpt %}
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
