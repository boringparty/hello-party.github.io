---
layout: page
title: Search
permalink: /search/
---

<div id="search-container">
 <input type="text" id="search-input" placeholder="Search through the blog posts...">
 <ul id="results-container"></ul>
</div>

<script src="{{ site.baseurl }}/assets/simple-jekyll-search.min.js" type="text/javascript"></script>
<ul>
<script>
 SimpleJekyllSearch({
 searchInput: document.getElementById('search-input'),
 resultsContainer: document.getElementById('results-container'),
 searchResultTemplate: '<li><a href="{url}">{title}</a></li></div>',
 json: '{{ site.baseurl }}/search.json'
 });
</script>
</ul>
