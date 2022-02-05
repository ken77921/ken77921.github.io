---
layout: page
title: projects
permalink: /projects/
description: A growing collection of cool projects.
nav: true
nav_order: 3
display_categories: [Nature Language Processing, Neural Network, Education, Computer Vision and Multimedia]
horizontal: false
display_grids: false
---


<!-- 020322[CY] -->

<!-- Computer Vision & Multimedia-->
<div class="row">
  <h2>Computer vision and multimedia</h2>
  <div class="col-4">
    <img src="../assets/img/proj12-cv-Superpixel-Based Large Displacement Optical Flow.png">
  </div>
  <div class="col">
    <h3>Superpixel-Based Large Displacement Optical Flow</h3>
    <p>
    We formulated our objective function at the superpixel level rather than the pixel level as the traditional optical flow method did.  
    Our method achieves better large displacement matching capability than LDOF in videos with lower quality , and has been accepted to ICIP 2013 (<a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_71ff29f7b6fc4c45822bb2e097dd0b45.pdf">Paper</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_4e98e9d181694a5f9724a6698a1dac98.pdf">Poster</a>).
    </p>
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
