---
layout: about
title: about
permalink: /
subtitle: >
  M.S. Student, Intelligent Systems & Robotics Lab<br>
  Korea University<br>
  Advisor: Prof. Woojin Chung

profile: false # add a profile image after replacing the placeholder content
selected_papers: false
social: true

announcements:
  enabled: false

latest_posts:
  enabled: false
---

<style>
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

  .soon-home__links a {
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

  .soon-home__links a:hover {
    border-color: var(--global-theme-color);
    color: var(--global-theme-color);
  }

  .soon-home__focus {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.8rem;
    margin: 0.8rem 0 1.9rem;
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

  .soon-home__more {
    font-size: 0.94rem;
  }

  @media (max-width: 768px) {
    .soon-home {
      max-width: none;
    }

    .soon-home__focus {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="soon-home">
  <p class="soon-home__lede">
    I am <strong>Soonhwan Kwon (권순환)</strong>, an M.S. student in the Intelligent Systems & Robotics Lab at Korea University, advised by Prof. Woojin Chung. My research interests are mobile robot perception and navigation, robot learning, and simulation.
  </p>

  <div class="soon-home__links" aria-label="Profile links">
    <a href="mailto:shk01421@korea.ac.kr">Email</a>
    <a href="https://github.com/Soon421">GitHub</a>
  </div>

  <div class="soon-home__focus" aria-label="Research interests">
    <div class="soon-home__focus-item">
      <strong>Mobile robot perception and navigation</strong>
      <span>Perception and navigation methods for mobile robotic systems.</span>
    </div>
    <div class="soon-home__focus-item">
      <strong>Robot learning and simulation</strong>
      <span>Learning-based robotics and simulation-based development and evaluation.</span>
    </div>
  </div>

  <p class="soon-home__more">
    More details will be added to <a href="{% link _pages/projects.md %}">projects</a> and <a href="{% link _pages/cv.md %}">CV</a>.
  </p>
</div>
