---
layout: page
title: 武器庫
permalink: /weapons/
---

ここに私が使っているAIツールの一覧を表示します。

{% for post in site.posts %}
  {% if post.categories contains 'tool' %}
  - [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y年%m月%d日" }}
  {% endif %}
{% endfor %}
