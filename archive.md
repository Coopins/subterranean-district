---
layout: page
title: Archive
permalink: /archive/
---

<p class="lede">
A growing record of stories, images, and observations from beneath the surface.
</p>

{% if site.posts.size > 0 %}
<div class="archive-page-grid">
  {% for post in site.posts %}
  <a href="{{ post.url | relative_url }}" class="archive-row">
    <div>
      <div class="archive-row-title">{{ post.title }}</div>
      {% if post.excerpt %}
        <div class="archive-row-excerpt">{{ post.excerpt | strip_html | truncate: 180 }}</div>
      {% endif %}
    </div>
    <div class="archive-row-meta">
      {{ post.date | date: "%b %-d, %Y" }}{% if post.categories and post.categories.size > 0 %}<br/>{{ post.categories | join: ", " }}{% endif %}
    </div>
  </a>
  {% endfor %}
</div>
{% else %}
<p class="small">The archive is quiet for now. Soon.</p>
{% endif %}
