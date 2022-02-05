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

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h4></h4>
    <p>
    </p>
  </div>
</div>


<!-- 02.22[CY] -->
<h2 style="color: #00369f">Natural Language Processing</h2>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj1-nlp-interactive_LM_first_figure.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h4>Multi-facet Embeddings for Controlling the Topics of Language Generation</h4>
    <p>
      We design a framework that displays multiple candidate upcoming topics, of which a user can select a subset to guide the generation. Our framework consists of two components: (1) a method that produces a set of candidate topics by predicting the centers of word clusters in the possible continuations, and (2) a text generation model whose output adheres to the chosen topics. The training of both components is self-supervised, using only unlabeled text. Our experiments demonstrate that our topic options are better than those of standard clustering approaches, and our framework often generates fluent sentences related to the chosen topics, as judged by automated metrics and crowdsourced workers.
      (<a href="http://arxiv.org/abs/2103.15335">Paper</a>, <a href="https://github.com/iesl/interactive_LM">Code</a>, <a href="https://slideslive.com/38954487/changing-the-mind-of-transformers-for-topicallycontrollable-language-generation">Talk</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_8212c213a26a4c36acc69989aec2399c.key?dn=EACL_interactive_LM.key">Slides</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_87e429adfcb9478e86a55033df144458.pdf">Poster</a>)
    </p>
  </div>
</div>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj2-nlp-Multi-facet Embeddings for Relation Extraction.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h4>Multi-facet Embeddings for Relation Extraction</h4>
    <p>
      We propose multi-facet universal schema that uses a neural model to represent each sentence pattern as multiple facet embeddings and encourage one of these facet embeddings to be close to that of another sentence pattern if they cooccur with the same entity pair. In our experiments, we demonstrate that multi-facet embeddings significantly outperform their single facet embedding counterpart, compositional universal schema (Verga et al., 2016), in distantly supervised relation extraction tasks. Moreover, we can also use multiple embeddings to detect the entailment relation between two sentence patterns when no manual label is available.
      (<a href="http://arxiv.org/abs/2103.15335">Paper</a>, <a href="https://github.com/iesl/interactive_LM">Code</a>, <a href="https://slideslive.com/38954487/changing-the-mind-of-transformers-for-topicallycontrollable-language-generation">Talk</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_8212c213a26a4c36acc69989aec2399c.key?dn=EACL_interactive_LM.key">Slides</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_97d81dbfca604d07b825f2214805166a.pdf">Poster</a>)
    </p>
  </div>
</div>


<!-- Neural Network -->
<h2 style="color: #00369f">Neural Network</h2>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj7-nn.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h4>Use Active Learning to Improve SGD [Better title?]</h4>
    <p>
    Inspired by active learning, we propose two alternatives to re-weight training samples based on lightweight estimates of sample uncertainty in stochastic gradient descent (SGD). Extensive experimental results on six datasets show that our methods reliably improve accuracy in various network architectures, including additional gains on top of other popular training techniques (<a href="https://arxiv.org/abs/1704.07433">Paper</a>, <a href="https://arxiv.org/abs/1704.07433">Poster</a>).
    </p>
  </div>
</div>


<!-- Education -->
<h2 style="color: #00369f">Education</h2>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj8-education-student modeling.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h4>Student Modeling and Prerequisite Verification in Knowledge Tree</h4>
    <p>
    We extract answering logs of the exercises from <a href="https://www.junyiacademy.org/">Junyi Academy</a>, an E-learning website similar to Khan Academy.
    </p>
    <p>
    We use crowdsourcing and machine learning to discover relationships between exercises. Based on that, we will design a mechanism of adaptive test to improve learning experiences of Junyi academy (<a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_059b30bf7b2444e7a8e0814baf9e1fd7.pdf">Paper</a>, <a href="https://f6d60bef-de96-4b94-b613-4913f88f2f0f.filesusr.com/ugd/e150d8_d281f5be254b434eb095cfc9d84cf75d.pptx?dn=Modeling%20Exercise%20Relationships%20in%20E-Learning_release.pptx">Presentation</a>, <a href="http://people.umass.edu/hawshiuancha/junyi_dependency_prediction.zip">Demo</a>, <a href="https://pslcdatashop.web.cmu.edu/DatasetInfo?datasetId=1198">Dataset</a>).
    </p>
  </div>
</div>

<!-- Computer Vision & Multimedia-->
<h2 style="color: #00369f">Computer Vision and Multimedia</h2>

<div class="row row-grid">
  <div class="col-4">
    <img src="../assets/img/proj9-cv-Active Sampling for estimating QoE model.png" class="img-responsive" width="100%">
  </div>
  <div class="col">
    <h4>Active Sampling for estimating QoE model</h4>
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
    <h4>Hierarchical Image Segmentation without Training</h4>
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
    <h4>Decomposi-tion of Multiple Foreground Co-segmentation</h4>
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
    <h4>Superpixel-Based Large Displacement Optical Flow</h4>
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
