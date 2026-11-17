---
title: Productions
permalink: /productions/
layout: single
classes: wide
excerpt: Selected productions and performance work.
toc: false
header:
  overlay_image: /assets/images/84fc40f0ce507c285a42cd0a8bfa10d9.jpeg
  overlay_filter: "0.8"
---

<div class="productions-grid">
  {% assign productions = site.productions | sort: "date" | reverse %}
  {% for post in productions %}
    <a href="{{ post.url | relative_url }}">
      <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title | escape }}">
      <div class="production-title">{{ post.title }}</div>
    </a>
  {% endfor %}
</div>


<style>
  .wide .page {
    float: none;
    width: 100%;
    padding-right: 0;
  }

  .productions-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0;
    margin: 0;
  }
  .productions-grid a { display: block; line-height: 0; position: relative; }
  .productions-grid img {
    display: block;
    width: 100%;
    aspect-ratio: 3 / 2;
    object-fit: cover;
    border-radius: 0;
    margin: 0;
  }
  .production-title {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 0.75em 1em;
    background: rgba(0, 0, 0, 0.5);
    color: #fff;
    line-height: 1.3;
    font-size: 0.95rem;
  }
</style>