---
layout: page
title: projects
permalink: /projects/
description: 주요 연구 및 개발 프로젝트
nav: true
nav_order: 2
---

<style>
  .soon-project-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1rem;
  }

  .soon-project-slot {
    position: relative;
    min-width: 0;
  }

  .soon-project-slot > .col {
    height: 100%;
    padding: 0;
  }

  .soon-project-slot--publication-text-only .card-body {
    padding-top: 3rem;
  }

  .soon-project-publication {
    position: absolute;
    z-index: 1;
    top: 0.75rem;
    left: 0.75rem;
    display: inline-flex;
    padding: 0.25rem 0.55rem;
    border-radius: 999px;
    background: var(--global-theme-color);
    color: #fff;
    font-size: 0.72rem;
    font-weight: 700;
    line-height: 1.2;
    pointer-events: none;
  }

  @media (max-width: 768px) {
    .soon-project-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<!-- pages/projects.md -->
<div class="projects">
{% assign sorted_projects = site.projects | sort: "date" | reverse %}
  <div class="soon-project-grid">
    {% for project in sorted_projects %}
    <div class="soon-project-slot{% if project.publications %} soon-project-slot--publication{% unless project.img %} soon-project-slot--publication-text-only{% endunless %}{% endif %}">
      {% if project.publications %}
        <span class="soon-project-publication">Publication</span>
      {% endif %}
      {% include projects.liquid %}
    </div>
    {% endfor %}
  </div>
</div>
