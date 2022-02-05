---
layout: page
title: projects
permalink: /projects/
description: A growing collection of cool projects.
nav: true
display_categories: [Natural language processing, Neural network, Education, Computer vision and multimedia]
horizontal: false
display_grids: false
---


<!-- 020322[CY] -->

<div class="row">
  <div class="col-4">
    <img src="assets/img/proj12-cv-Superpixel-Based Large Displacement Optical Flow.png">
  </div>
  <div class="col">
    <h3>Superpixel-Based Large Displacement Optical Flow</h3>
  </div>
</div>
<div class="row">
  <div class="col">
    1 of 3
  </div>
  <div class="col">
    2 of 3
  </div>
  <div class="col">
    3 of 3
  </div>
</div>


<!-- [Grids] pages/projects.md -->
<div class="projects">
 {%- if page.display_grids %} 
  {%- if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {%- for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    {%- assign categorized_projects = site.projects | where: "category", category -%}
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
    {%- assign sorted_projects = site.projects | sort: "importance" -%}
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
