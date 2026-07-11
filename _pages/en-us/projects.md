---
page_id: projects
layout: page
title: projects
permalink: /projects/
description: Research projects, software, datasets, and benchmarks.
nav: true
nav_order: 3
display_categories: [research, software]
horizontal: true
---

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
      <a id="{{ site.data[site.active_lang].strings.categories[category] }}" href=".#{{ site.data[site.active_lang].strings.categories[category] }}">
        <h2 class="category">{{ site.data[site.active_lang].strings.categories[category] }}</h2>
      </a>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.liquid %}
          {% endfor %}
        </div>
      </div>
    {% endfor %}
  {% endif %}
</div>
