---
title: Productions
permalink: /productions/
layout: single
excerpt: Selected productions and performance work.
toc: false
header:
  overlay_image: /assets/images/84fc40f0ce507c285a42cd0a8bfa10d9.jpeg
  overlay_filter: "0.8"
---
{% assign productions = site.productions | sort: "date" | reverse %} {% for post in productions %}

![{{ post.title | escape }}](<{{ post.header.teaser | relative_url }}>)

[{{ post.title }}]({{ post.url | relative_url }})

 {% endfor %}

