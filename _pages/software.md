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
Natural Language Processing

<!-- 02.22[CY] -->
<div class="div-cat-header">
  <h2>Natural Language Processing</h2>
</div>
<div>
  <h4>Multi-facet Embeddings</h4>
  <div>
    <p>
    Interactive Language Generation <a href="https://github.com/iesl/interactive_LM">(PyTorch and python)</a><br>
    Multi-facet Relation Extraction <a href="https://github.com/rohanpaul11/multifacet-re">(PyTorch and python)</a>
    </p>
  </div>
</div>

<div>
  <p>
  <h4>Unsupervised Hypernym Detection</h4>
  <div>
    <p>Distributional Inclusion Vector Embedding <a href="https://github.com/iesl/Distributional-Inclusion-Vector-Embedding">(tensorflow and python)</a></p>
  </div>
</div>

<div class="row row-grid">
  <h4>Educational Data Mining</h4>
  <p>Demo code to visualize predicted exercise relationships <a href="">(GAE for python)</a>
  </p>
</div>


<!-- 02.22[CY] -->
<div class="div-cat-header">
  <h2>Computer Vision and Multimedia</h2>
</div>

<div class="row row-grid">
  <h4>Unsupervised Segmentation</h4>
  <p>
    Hierarchical Image Segmentation without Training <a href="http://mml.citi.sinica.edu.tw/papers/HDC_code_ACCV_2014/">(Matlab)</a><br>
    Mutiple Foreground Cosegmentation Decomposition <a href="http://mml.citi.sinica.edu.tw/papers/MFC_code_CVIU_2015">(Matlab)</a><br>
    Efficient Hierarchical Graph-based Video Segmentation <a href="http://mml.citi.sinica.edu.tw/papers/GBH_code_ACCV_2014">(C/C++ for Windows)</a><br>
    ~10 times faster than the original from <a href="https://cse.buffalo.edu/~jcorso/r/supervoxels/">LIBSVX</a>
  </p>
</div>

<div class="row row-grid">
  <h4>Clustering</h4>
  <p>
    Efficient Kmeans Using Multiple Threads <a href="">(C/C++ with Matlab wrapper)</a>
    ~3 times faster than Matlab statistical toolbox<br>
    Efficient GMM Using Multiple Threads <a href="">(C/C++ with Matlab wrapper)</a><br>
    ~6 times faster than Matlab statistical toolbox
  </p>
</div>

<div class="row row-grid">
  <h4>Optical Flow</h4>
  <p>
    Superpixel-Based Large Displacement Optical Flow <a href="http://mml.citi.sinica.edu.tw/papers/SPLDOF_code.php">(Matlab)</a>
  </p>
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
