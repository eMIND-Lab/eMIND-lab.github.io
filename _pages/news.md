---
layout: page
title: News
permalink: /news/
description: Latest news and updates from E-MIND Lab
nav: true
nav_order: 5
---

{% assign news = site.news | reverse %}
{% for item in news %}
  {{ item.content }}
  <p class="post-meta">{{ item.date | date: "%B %d, %Y" }}</p>
  {% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
