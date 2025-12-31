---
layout: default
title:
description: The district beneath the surface.
---

<p class="small">A living archive</p>

# Subterranean District

<p class="lede">
Culture, identity, city life, and underground storytelling — documented honestly, with intention.
</p>

<p class="small">
<a href="{{ '/manifesto/' | relative_url }}">Manifesto</a> ·
<a href="{{ '/archive/' | relative_url }}">Archive</a> ·
<a href="{{ '/about/' | relative_url }}">About</a>
</p>

## Orientation

Subterranean District exists to observe what often goes unnoticed — the spaces between movements, the people outside the spotlight, the ideas forming quietly before they surface.

This is a place for attention. For patience. For work that values depth over immediacy.

## From the Manifesto

> The underground is not a fringe.  
> It is the foundation.  
> The blueprint for what comes next.

<p class="small">
<a href="{{ '/manifesto/' | relative_url }}">Read the full manifesto →</a>
</p>

## Latest Entries

{% if site.posts and site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts limit: 3 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta">
      {{ post.date | date: "%B %-d, %Y" }}
    </span>

    {% if post.excerpt %}
      <p class="small">{{ post.excerpt | strip_html | truncate: 160 }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>

<p class="small">
<a href="{{ '/archive/' | relative_url }}">Enter the archive →</a>
</p>
{% else %}
<p class="small">
The archive is quiet for now. Soon.
</p>
{% endif %}

<p class="lede">
The story beneath the story.
</p>

<p class="small">
A publication for what survives below the surface.
</p>
