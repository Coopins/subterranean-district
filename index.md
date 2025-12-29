---
layout: default
title:
description: The district beneath the surface.
---

<p class="small">A living archive</p>

# The district beneath the surface.

<p class="lede">
Culture, identity, city life, and underground storytelling — documented honestly, with intention.
</p>

<p>
<a href="/manifesto/">Manifesto</a> &nbsp;·&nbsp;
<a href="/archive/">Archive</a> &nbsp;·&nbsp;
<a href="/about/">About</a>
</p>

<hr>

## Manifesto

<blockquote>
  <p>
    Subterranean District was born in the spaces most people ignore — the alleys, basements, late-night corridors,
    and the quiet interiors of ordinary lives. We document what survives beneath the surface.
  </p>
</blockquote>

<p class="small">
  <a href="/manifesto/">Read the full manifesto →</a>
</p>

<hr>

## Latest

{% if site.posts and site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts limit: 5 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta">
      {{ post.date | date: "%B %-d, %Y" }}
      {% if post.categories and post.categories.size > 0 %}
        · {{ post.categories | join: ", " }}
      {% endif %}
    </span>

    {% if post.excerpt %}
      <p class="small">{{ post.excerpt | strip_html | truncate: 180 }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>

<p class="small">
  <a href="/archive/">Open the archive →</a>
</p>
{% else %}
<p class="small">
  The archive is quiet for now. Soon.
</p>
{% endif %}

<hr>

## About

<p class="lede">
Subterranean District is a publication devoted to the overlooked — the intimate, the urban, the hidden.
</p>

<p class="small">
  <a href="/about/">Read more →</a>
</p>
