---
layout: page
title: Archive
permalink: /archive/
---

<p class="sd-archive-intro">
  A growing record of stories, images, and observations from beneath the surface.
</p>

<ul class="sd-archive-list">
  {% for post in site.posts %}
    <li class="sd-archive-item">
      <span class="sd-archive-year">{{ post.date | date: "%Y" }}</span>
      <span class="sd-archive-title"><a href="{{ post.url }}">{{ post.title }}</a></span>
    </li>
  {% endfor %}
</ul>
