---
layout: page
permalink: /categories/
title: Categories
---

<div id="archives">
 {% assign categories = site.categories | sort %}
 {% for category in site.categories %}
  <div class="archive-group">
{% capture category_name %}{{ category | first }}{% endcapture %}
<div id="#{{ category_name | slugize }}"></div>
<h3 class="category-head">{{ category_name }}</h3>

   <ul>
{% for post in site.categories[category_name] %}
<article class="archive-item">
<li><a href="{{ site.baseurl }}{{ post.url }}">{% if post.title and post.title != "" %}{{post.title}}{%endif%}</a></li>
</article>
{% endfor %}
   </ul></div>
{% endfor %}
</div>
