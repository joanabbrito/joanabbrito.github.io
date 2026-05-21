---
layout: page
permalink: /repositories/
title: repositories
description: A selection of my open-source projects.
nav: true
nav_order: 3
---

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2">
    {% for repo in site.data.repositories.repos %}
    <div class="col mb-4">
      <a href="{{ repo.url }}" target="_blank" style="text-decoration: none; color: inherit;">
        <div class="card h-100 hoverable">
          {% if repo.img %}
            <img src="{{ repo.img | prepend: '/assets/img/' | relative_url }}" class="card-img-top" alt="{{ repo.name }}" style="object-fit: cover; height: 200px;">
          {% endif %}
          <div class="card-body">
            <h5 class="card-title">{{ repo.name }}</h5>
            <p class="card-text">{{ repo.description }}</p>
          </div>
        </div>
      </a>
    </div>
    {% endfor %}
  </div>
</div>
