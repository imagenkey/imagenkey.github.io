---
layout: page
title: 記事アーカイブ - Archive
---

## 投稿した記事の一覧

これまでに投稿した「武器」や「考察」の記録です。

{% for post in site.posts %}
  - [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y年%m月%d日" }})
{% endfor %}
