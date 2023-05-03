---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013]
nav: true
title_order: 10
---
<!-- _pages/publications.md -->
<div class="publications">
My <a href="https://www.semanticscholar.org/author/144827671">Semantic Scholar</a> and <a href="https://scholar.google.com/citations?user=fdGXVd4AAAAJ">Google Scholar</a> pages


{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
