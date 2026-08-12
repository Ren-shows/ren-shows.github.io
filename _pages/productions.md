---
title: Productions
permalink: /productions/
layout: single
classes: wide
excerpt: Selected productions and performance work.
toc: false
header:
  overlay_image: /assets/images/84fc40f0ce507c285a42cd0a8bfa10d9.jpeg
  overlay_filter: "0.4"
---

<style>
  /* Wide layout still floats .page right at reduced width, leaving a gap on
     the left. Reset it so the content is truly full-width and centered. */
  .wide .page {
    float: none;
    width: 100%;
    padding-right: 0;
  }

  /* Two-across, edge-to-edge production gallery. */
  .productions-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0;
    margin: 0;
  }
  .productions-grid a { display: block; line-height: 0; }
  .productions-grid img {
    display: block;
    width: 100%;
    aspect-ratio: 3 / 2;
    object-fit: cover;
    border-radius: 0;
    margin: 0;
  }
</style>

<div class="productions-grid">
  {% assign productions = site.productions | sort: "date" | reverse %}
  {% for post in productions %}
    <a href="{{ post.url | relative_url }}">
      <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title | escape }}">
    </a>
  {% endfor %}
</div>
