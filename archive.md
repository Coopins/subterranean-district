---
layout: page
title: Archive
permalink: /archive/
---

<p class="lede">
A growing record of stories, images, and observations from beneath the surface.
</p>

{% if site.posts and site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta">
      {{ post.date | date: "%B %-d, %Y" }}
      {% if post.categories and post.categories.size > 0 %}
        · {{ post.categories | join: ", " }}
      {% endif %}
    </span>

    {% if post.excerpt %}
      <p class="small">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="small">The archive is quiet for now. Soon.</p>
{% endif %}
