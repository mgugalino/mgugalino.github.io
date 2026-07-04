---
layout: page
title: projects
permalink: /projects/
description: I run large-scale simulations of astrophysical objects and run analysis pipelines that transform these data products into synthetic observables that can be compared to real-world measurements.
nav: true
nav_order: 3
display_categories: [Active, Past]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">

{% if site.enable_project_categories and page.display_categories %}

  {% for category in page.display_categories %}

    {% assign categorized_projects = site.projects
      | where: "category", category
      | sort: "importance" %}

    {% if categorized_projects.size > 0 %}

    <section class="project-group" id="{{ category | slugify }}">
      <h2 class="project-header">{{ category }}</h2>

      {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
          {% for project in categorized_projects %}
            {% include projects_horizontal.liquid %}
          {% endfor %}
        </div>
      </div>
      {% else %}
      <div class="row row-cols-1 row-cols-md-3">
        {% for project in categorized_projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
      {% endif %}

    </section>

    {% endif %}

  {% endfor %}

{% else %}

  {% assign sorted_projects = site.projects | sort: "importance" %}

  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}

{% endif %}

</div>