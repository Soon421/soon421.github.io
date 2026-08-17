---
layout: about
title: about
permalink: /
subtitle: >
  M.S. Student, Intelligent Systems & Robotics Lab<br>
  Korea University<br>
  Advisor: Prof. Woojin Chung

profile:
  align: right
  image: soonhwan-kwon.jpg
  image_circular: false
selected_papers: false
social: true

announcements:
  enabled: false

latest_posts:
  enabled: false
---

<style>
  html {
    scroll-behavior: smooth;
  }

  .soon-home {
    max-width: 720px;
  }

  .soon-home__lede {
    margin: 0.45rem 0 0.9rem;
    font-size: 1.01rem;
    line-height: 1.7;
  }

  .soon-home__links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin: 1rem 0 1.6rem;
  }

  .soon-home__link {
    display: inline-flex;
    align-items: center;
    min-height: 2rem;
    padding: 0.38rem 0.7rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.4rem;
    color: var(--global-text-color);
    background: var(--global-card-bg-color);
    font-size: 0.9rem;
    font-weight: 600;
    line-height: 1.2;
    text-decoration: none;
  }

  a.soon-home__link:hover {
    border-color: var(--global-theme-color);
    color: var(--global-theme-color);
  }

  .soon-home__link--disabled {
    color: var(--global-text-color-light);
  }

  .soon-home__section {
    scroll-margin-top: 5.5rem;
  }

  .soon-home__focus {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 0.8rem;
    margin: 0.4rem 0 1.9rem;
  }

  .soon-home__focus-title {
    margin: 0 0 0.4rem;
    font-size: 1.2rem;
  }

  .soon-home__focus-item {
    padding: 0.8rem 0 0.3rem;
    border-top: 1px solid var(--global-divider-color);
  }

  .soon-home__focus-item strong {
    display: block;
    margin-bottom: 0.3rem;
    color: var(--global-text-color);
    font-size: 0.96rem;
    line-height: 1.4;
  }

  .soon-home__focus-item span {
    color: var(--global-text-color-light);
    font-size: 0.9rem;
    line-height: 1.55;
  }

  .soon-home__projects-title {
    margin: 0 0 0.8rem;
    font-size: 1.2rem;
  }

  .soon-home__project-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1rem;
  }

  .soon-home__project-slot {
    position: relative;
    min-width: 0;
  }

  .soon-home__project-slot > .col {
    height: 100%;
    padding: 0;
  }

  .soon-home__project-slot--publication-text-only .card-body {
    padding-top: 3rem;
  }

  .soon-home__publication-badge {
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

  .soon-home__empty {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.94rem;
  }

  @media (max-width: 768px) {
    .soon-home {
      max-width: none;
    }

    .soon-home__focus {
      grid-template-columns: 1fr;
    }

    .soon-home__project-grid {
      grid-template-columns: 1fr;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    html {
      scroll-behavior: auto;
    }
  }
</style>

{% comment %}
TODO(portfolio): Once the research direction becomes more concrete, add a one-sentence research goal after the introduction.
Candidate: "My goal is to build autonomous mobile robots that can operate reliably in complex real-world environments by integrating navigation, simulation, and learning."
{% endcomment %}

<div id="about" class="soon-home soon-home__section">
  <p class="soon-home__lede">
    I am <strong>Soonhwan Kwon (권순환)</strong>, an M.S. student in the Intelligent Systems & Robotics Lab at Korea University, advised by Prof. Woojin Chung. My research interests lie in mobile robot navigation, simulation-based robotics, and learning-based robotics.
  </p>

  <div class="soon-home__links" aria-label="Profile links">
    <a class="soon-home__link" href="mailto:shk01421@korea.ac.kr">Email</a>
    <a class="soon-home__link" href="https://github.com/Soon421">GitHub</a>
    <span id="cv" class="soon-home__link soon-home__link--disabled soon-home__section" aria-disabled="true">CV (PDF) · Coming soon</span>
  </div>

  <section id="research" class="soon-home__section" aria-labelledby="research-title">
    <h2 id="research-title" class="soon-home__focus-title">Research Areas</h2>

    <div class="soon-home__focus" aria-label="Research interests">
      <div class="soon-home__focus-item">
        <strong>Mobile robot navigation</strong>
        <span>Localization, planning, and control for autonomous mobile robots operating in complex real-world environments.</span>
      </div>
      <div class="soon-home__focus-item">
        <strong>Simulation-based robotics</strong>
        <span>NVIDIA Isaac Sim environments, ROS 2 integration, simulation-based learning, and system-level evaluation.</span>
      </div>
      <div class="soon-home__focus-item">
        <strong>Learning-based robotics</strong>
        <span>Multimodal learning, world models, robot policy learning, and vision-language-action models.</span>
      </div>
    </div>

  </section>

  <section id="projects" class="soon-home__section" aria-labelledby="projects-title">
    <h2 id="projects-title" class="soon-home__projects-title">Projects</h2>

    {% assign sorted_projects = site.projects | sort: "date" | reverse %}
    {% if sorted_projects.size > 0 %}
    <div class="projects">
      <div class="soon-home__project-grid">
        {% for project in sorted_projects %}
        <div class="soon-home__project-slot{% if project.publications %} soon-home__project-slot--publication{% unless project.img %} soon-home__project-slot--publication-text-only{% endunless %}{% endif %}">
          {% if project.publications %}
            <span class="soon-home__publication-badge">Publication</span>
          {% endif %}
          {% include projects.liquid %}
        </div>
        {% endfor %}
      </div>
    </div>
    {% else %}
      <p class="soon-home__empty">Projects will be added as they are documented.</p>
    {% endif %}

  </section>
</div>

<script>
  const soonHomeMenu = document.getElementById("navbarNav");
  const soonHomeMenuToggle = document.querySelector('[data-nav-toggle="navbarNav"]');

  document.querySelectorAll('#navbarNav a[href^="/#"]').forEach((link) => {
    link.addEventListener("click", () => {
      soonHomeMenu?.classList.remove("show");
      soonHomeMenuToggle?.classList.add("collapsed");
      soonHomeMenuToggle?.setAttribute("aria-expanded", "false");
    });
  });
</script>
