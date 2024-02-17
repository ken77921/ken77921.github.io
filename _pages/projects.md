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
$blue-color-dark: #666699
---

<h2 style="color: #666699">Natural Language Processing</h2>

<h2 style="color: #666699">Neural Network</h2>

<h2 style="color: #666699">Education</h2>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h3></h3>
    <p>
    </p>
  </div>
</div>


<!-- 020322[CY] -->

<!-- Computer Vision & Multimedia-->
<h2 style="color: #00369f">Computer Vision and Multimedia</h2>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj9-cv-Active Sampling for estimating QoE model.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h3>Active Sampling for estimating QoE model</h3>
    <p>
    We use Bayesian learning to model the non-linear relationships between quality of experience (QoE) and multiple factors.
    </p>
    <p>
    Our experiment shows that active sampling can be used to reduce the number of samples collected from crowdsourcing for building such model (<a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_50ae23ac1a7f4a46a4b3065b26f0c84a.pdf">Paper</a>).
    </p>
  </div>
</div>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj10-cv-Hierarchical Image Segmentation without Training.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h3>Hierarchical Image Segmentation without Training</h3>
    <p>
    We proposed a general framework which applies classifiers with different complexity to discriminate segments in an image.
    </p>
    <p>
    Our unsupervisedhierarchical segmentation results achieve similar or better performance in several standard benchmarks compared with the current state-of-the-art methods based on learning, and has been accepted to ACCV 2014 (<a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_242e704833024ea4a6723dfd884e85ff.pdf">Paper</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_f6c41538d19a4788a7efd64ffcfd01be.pdf">Poster</a>).
  </p>
  </div>
</div>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj11-cv-Decomposition of Multiple Foreground Co-segmentation.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h3>Decomposi-tion of Multiple Foreground Co-segmentation</h3>
    <p>
    We proposed an efficient algorithm which decomposes the unsupervised Multiple Foreground Co-segmentation problem into three sub-problems: segmentation, matching and figure-ground classification.
    </p>
    <p>
    Our method improves the accuracy of the state-of-the-art method by 13% in a standard benchmark, and has been accepted by CVIU (<a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_6e352dd41985407bb5db08b256f1d333.pdf">Paper</a>)
    </p>
  </div>
</div>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj12-cv-Superpixel-Based Large Displacement Optical Flow.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h3>Superpixel-Based Large Displacement Optical Flow</h3>
    <p>
    We formulated our objective function at the superpixel level rather than the pixel level as the traditional optical flow method did.</p>
    <p>
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
