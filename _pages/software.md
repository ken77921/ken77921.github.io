---
layout: page
title: Software
permalink: /software/
description:
nav: true
nav_order: 4
display_categories: [Recommendation, Natural Language Processing, Computer Vision and Multimedia]
horizontal: false
display_grids: false
title_order: 100
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
  <h2>Recommendation</h2>
</div>
<div>
  <h4>Multi-facet Embeddings for Sequential Recommendation</h4>
  <div>
    <ul style="list-style-type:circle;">
    <li>Better Output Softmax Alternatives for SASRec and GRU4Rec <a href="https://github.com/iesl/softmax_CPR_recommend">(PyTorch, RecBole, and python)</a></li>
    </ul>
  </div>    
</div>
<br>

<hr>  
<div class="div-cat-header">
  <h2>Natural Language Processing</h2>
</div>

<div>
  <h4>Infinitely Large Language Model</h4>
  <div>
    <ul style="list-style-type:circle;">
      <li>Decoding Methods that Improve Factuality and Diversity (if you have multiple LLMs with different sizes) <a href="https://github.com/amazon-science/llm-asymptotic-decoding/">(PyTorch and python)</a></li>
    </ul>
  </div>
</div>

<div>
  <h4>Multi-facet Embeddings</h4>
  <div>
    <ul style="list-style-type:circle;">
      <li>Better Output Softmax Alternatives for LM <a href="https://github.com/iesl/Softmax-CPR">(PyTorch and python)</a></li>
      <li>Efficient BERT Ensembling <a href="https://github.com/iesl/multicls/">(PyTorch and python)</a></li>
      <li>Paper-Reviewer Affinity Estimation <a href="https://github.com/openreview/openreview-expertise">(PyTorch and python)</a> <a href="https://arxiv.org/pdf/2303.16750.pdf">(a third party evaluation)</a> </li>
      <li>Interactive Language Generation <a href="https://github.com/iesl/interactive_LM">(PyTorch and python)</a></li>
      <li>Multi-facet Relation Extraction <a href="https://github.com/rohanpaul11/multifacet-re">(PyTorch and python)</a></li>
    </ul>
  </div>
</div>

<div>
  <h4>Unsupervised Hypernym Detection</h4>
  <div>
    <ul style="list-style-type:circle;">
      <li>Distributional Inclusion Vector Embedding <a href="https://github.com/iesl/Distributional-Inclusion-Vector-Embedding">(tensorflow and python)</a></li>
    </ul>
  </div>
</div>
<br>

<hr> 

<div class="div-cat-header">
  <h2>Machine Learning</h2>
</div>
<div>
  <h4>Clustering</h4>
  <div>
  <ul style="list-style-type:circle;">
    <li>Efficient Kmeans Using Multiple Threads <a href="https://www.mathworks.com/matlabcentral/fileexchange/47737-kmeans_mt?s_tid=srchtitle_support_results_2_k-means%20thread">(C/C++ with Matlab wrapper)</a></li>
    ~3 times faster than Matlab statistical toolbox<br>
    <li>Efficient GMM Using Multiple Threads <a href="https://www.mathworks.com/matlabcentral/fileexchange/47741-gmm_mt?s_tid=srchtitle">(C/C++ with Matlab wrapper)</a></li>
    ~6 times faster than Matlab statistical toolbox
  </ul>
  </div>
  <h4>Educational Data Mining</h4>
  <div>
    <ul style="list-style-type:circle;">
      <li>Demo code to visualize predicted exercise relationships <a href="https://drive.google.com/file/d/1V5nEwmVkPclj_ZR-bKt9xzW7ApT6ZJo-/view?usp=sharing">(GAE for python)</a></li>
      <li>Predicting exercise relationships <a href="../assets/pdf/junyi_exer_relationship_released.zip">(R and python)</a></li>
    </ul>
  </div>
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
