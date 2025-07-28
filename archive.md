---
layout: page
title: "📚 研究アーカイブ"
permalink: /archive/
---

# 🗂️ 技術研究ログ完全版

これまでの全ての研究記録、実験結果、技術的洞察をクロノロジカルに整理。AI技術の進歩と共に蓄積された知見の宝庫です。

---

## 📊 統計サマリー

- **総記事数**: {{ site.posts.size }}件
- **カテゴリー数**: {{ site.categories.size }}種類
- **記録開始**: {{ site.posts.last.date | date: "%Y年%m月" }}

---

## 📝 全記録一覧

<div class="archive-list">
{% for post in site.posts %}
<div class="post-preview">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <div class="post-meta">
    <span class="date">{{ post.date | date: "%Y年%m月%d日" }}</span>
    {% if post.categories.size > 0 %}
    <span class="categories">
      {% for category in post.categories %}
        <span class="category-tag">{{ category }}</span>
      {% endfor %}
    </span>
    {% endif %}
  </div>
  {% if post.excerpt %}
  <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
  {% endif %}
</div>
{% endfor %}
</div>

---

## 🏷️ カテゴリー別索引

{% for category in site.categories %}
<div class="category-section">
  <h3>{{ category[0] | capitalize }}</h3>
  <ul>
  {% for post in category[1] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%Y/%m/%d" }}</li>
  {% endfor %}
  </ul>
</div>
{% endfor %}

---

*研究は継続中。新しい発見と洞察を随時追加していきます。*
