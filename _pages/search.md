---
layout: page
permalink: /search/
title: search
description:
nav: true
nav_order: 5
---

<!-- HTML search field -->
<div id="search-container">
  <input type="text" id="search-input" placeholder="Type your search here..." autofocus>
  <ul id="results-container"></ul>
</div>

<!-- Grab search-script.js -->
<script src="/assets/js/simple-jekyll-search.min.js" type="text/javascript"></script>

<!-- Configuration -->
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '/search.json',
    searchResultTemplate: '<li><a href="{url}">{title}</a><br><span class="post-meta">{date}</span></li>'
  })
</script>