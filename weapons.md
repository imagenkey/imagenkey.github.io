---
layout: page
title: 武器庫
permalink: /weapons/
---

最前線から引退した武器たちの記録です。それぞれの武器との思い出や、なぜ引退することになったのかなどを記録しています。

## 引退した武器たち

{% for post in site.posts %}
  {% if post.categories contains 'tool' and post.tags contains 'retired' %}
  - [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y年%m月%d日" }}
  {% endif %}
{% endfor %}

## 実験中だった武器たち

{% for post in site.posts %}
  {% if post.categories contains 'tool' and post.tags contains 'experimental' %}
  - [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y年%m月%d日" }}
  {% endif %}
{% endfor %}
