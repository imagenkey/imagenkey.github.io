---
layout: page
title: 武器庫
permalink: /weapons/
---

最前線から引退した武器たちと、実験段階で終わった武器たちの記録です。

## 引退・実験記録

{% for post in site.posts %}
  {% if post.categories contains 'tool' %}
  - [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y年%m月%d日" }}
  {% endif %}
{% endfor %}
