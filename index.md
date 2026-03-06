---
layout: default
title:
description: The district beneath the surface.
---

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">A Living Archive</div>
    <h1>Sub<em>terra</em><br/>nean<br/>District</h1>
    <p class="hero-sub">
      Culture, identity, and city life documented from beneath the surface.
      The scenes that form before anyone is watching. The voices that exist
      outside the spotlight.
    </p>
    <a href="{{ '/archive/' | relative_url }}" class="hero-cta">Enter the Archive</a>
  </div>
  <div class="hero-right">
    <div class="hero-right-content">
      <div class="large-quote">
        "The most interesting things happening in the world rarely appear in the spotlight first."
      </div>
    </div>
  </div>
</section>

<!-- SECTION HEADER -->
<div class="section-header">
  <span class="section-label">From the Manifesto</span>
  <span class="section-num">&sect; 01</span>
</div>

<!-- MANIFESTO STRIP -->
<section class="manifesto-strip">
  <div class="manifesto-aside">
    <div class="manifesto-label">Manifesto</div>
  </div>
  <div class="manifesto-body">
    <p>
      Subterranean District was born in the spaces <em>most people ignore.</em>
    </p>
    <p>
      The alleys. The basements. The late-night corridors.
      The rooms where conversations happen after the lights go out.
    </p>
    <p>
      It exists to document the culture that develops in those places &mdash;
      not the polished version. The real one.
    </p>
    <a href="{{ '/manifesto/' | relative_url }}" class="manifesto-link">Read the full manifesto</a>
  </div>
</section>

<!-- SECTION HEADER -->
<div class="section-header">
  <span class="section-label">Latest Entries</span>
  <span class="section-num">&sect; 02</span>
</div>

<!-- ARCHIVE GRID -->
<section class="archive-section">
  <div class="archive-grid">
    {% if site.posts.size > 0 %}
      {% assign featured = site.posts.first %}
      <a href="{{ featured.url | relative_url }}" class="archive-card featured">
        <div class="card-tag">Featured &middot; {{ featured.date | date: "%b %Y" }}</div>
        <h2 class="card-title">{{ featured.title }}</h2>
        {% if featured.excerpt %}
          <p class="card-excerpt">{{ featured.excerpt | strip_html | truncate: 160 }}</p>
        {% endif %}
        <div class="card-meta">{{ featured.date | date: "%B %-d, %Y" }}{% if featured.categories %} &middot; {{ featured.categories | join: ", " }}{% endif %}</div>
      </a>
      {% for post in site.posts offset:1 limit:4 %}
        <a href="{{ post.url | relative_url }}" class="archive-card">
          {% if post.category %}<div class="card-tag">{{ post.category }}</div>{% elsif post.categories and post.categories.size > 0 %}<div class="card-tag">{{ post.categories.first }}</div>{% endif %}
          <h2 class="card-title">{{ post.title }}</h2>
          {% if post.excerpt %}<p class="card-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>{% endif %}
          <div class="card-meta">{{ post.date | date: "%B %-d, %Y" }}</div>
        </a>
      {% endfor %}
    {% else %}
      <div class="archive-card featured">
        <div class="card-tag">Coming Soon</div>
        <h2 class="card-title">The archive is being built.</h2>
        <p class="card-excerpt">The district is being mapped. First entries arriving soon.</p>
        <div class="card-meta">The district beneath the surface</div>
      </div>
    {% endif %}
  </div>
</section>

<!-- QUOTE BAND -->
<div class="quote-band">
  <div class="quote-text">
    &ldquo;The underground is not a fringe.<br/>It is the foundation.<br/>The blueprint for what comes next.&rdquo;
  </div>
  <div class="quote-attr">&mdash; Subterranean District Manifesto</div>
</div>

<!-- ABOUT STRIP -->
<section class="about-strip">
  <div class="about-left">
    <div class="section-title">A document,<br/>not a <em>brand.</em></div>
    <p class="body-text">
      Subterranean District is an independent cultural publication and digital archive
      focused on documenting the parts of culture that exist beneath the surface of
      mainstream attention.
    </p>
    <p class="body-text">
      It does not chase trends. It does not sanitize stories.
      It observes them before they become trends, and presents them honestly.
    </p>
  </div>
  <div class="about-right">
    <div class="section-title" style="font-size:clamp(1.2rem,2.5vw,1.9rem);color:var(--fog);">
      The project treats overlooked subjects with seriousness and respect &mdash;
      <em>not as novelty or spectacle.</em>
    </div>
    <a href="{{ '/about/' | relative_url }}" class="manifesto-link" style="margin-top:3rem;display:inline-flex;">
      About the publication
    </a>
  </div>
</section>

<!-- TICKER -->
<div class="ticker">
  <div class="ticker-inner">
    <span>Subterranean District</span>
    <span>A Living Archive</span>
    <span>Culture &amp; Identity</span>
    <span>City Life After Dark</span>
    <span>Underground Storytelling</span>
    <span>Documented Honestly</span>
    <span>Subterranean District</span>
    <span>A Living Archive</span>
    <span>Culture &amp; Identity</span>
    <span>City Life After Dark</span>
    <span>Underground Storytelling</span>
    <span>Documented Honestly</span>
  </div>
</div>
