---
layout: page
title: software
permalink: /software/
description: A growing collection of cool software/tools.
nav: true
display_categories: [Natural Language Processing, Computer Vision and Multimedia]
horizontal: false
display_grids: false
---
<!--
<div class="row row-grid">
  <h4></h4>
  <p>
  </p>
</div>
-->

<!-- 02.22[CY] -->
<div class="div-cat-header">
  <h2>Natural Language Processing</h2>
</div>
<div class="row row-grid">
  <h4>Multi-facet Embeddings</h4>
  <p>
    <h3 style="text-align: left; color: #666699">Interactive Language Generation</h3><a href="https://github.com/iesl/interactive_LM">(PyTorch and python)</a>
  </p>
  <p>
    <h3 style="text-align: left; color: #666699">Multi-facet Relation Extraction</h3> <a href="https://github.com/rohanpaul11/multifacet-re">(PyTorch and python)</a>
  </p>
</div>


<!-- 02.22[CY] -->
<div class="div-cat-header">
  <h2>Computer Vision and Multimedia</h2>
</div>


<!-- [Grids] pages/sw.md -->
<div class="projects">
{%- if page.display_grids %}
  {%- if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {%- for category in page.display_categories %}
    <h2 class="category" style="text-align: left; color: #00369f">{{ category }}</h2>
    
    <!-- CY 01.24.21: new sw collection -->
    {%- assign categorized_projects = site.projects | where: "category", category -%}
    <!-- {%- assign categorized_projects = site.projects | where: "category", category -%} -->

    {%- assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal -%}
    <div class="container">
      <div class="row row-cols-2">
      {%- for project in sorted_projects -%}
        {% include projects_horizontal.html %}
      {%- endfor %}
      </div>
    </div>
    {%- else -%}
    <div class="grid">
      {%- for project in sorted_projects -%}
        {% include projects.html %}
      {%- endfor %}
    </div>
    {%- endif -%}
    {% endfor %}

  {%- else -%}
  <!-- Display projects without categories -->
    {%- assign sorted_projects = site.software | sort: "importance" -%}
    <!-- Generate cards for each project -->
    {% if page.horizontal -%}
    <div class="container">
      <div class="row row-cols-2">
      {%- for project in sorted_projects -%}
        {% include projects_horizontal.html %}
      {%- endfor %}
      </div>
    </div>
    {%- else -%}
    <div class="grid">
      {%- for project in sorted_projects -%}
        {% include projects.html %}
      {%- endfor %}
    </div>
    {%- endif -%}
  {%- endif -%}
{% endif %}
</div>
