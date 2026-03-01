---
layout: page
permalink: /repositories/
title: repositories & code
description: Open-source projects, code samples, and GitHub contributions showcasing architecture, frameworks, and tools.
nav: true
nav_order: 4
---

A collection of my GitHub repositories, including open-source projects, code samples, and architectural frameworks.

## GitHub Profile

Explore my repositories on GitHub showcasing:
- Open-source frameworks and libraries
- Reference implementations for architectural patterns
- Developer tools and utilities
- Learning resources and tutorials
- Internal platform engineering components

{% if site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

## Featured Projects

Check out some of my highlighted repositories showcasing modern development practices:

- **Microservices Frameworks** – Production-ready service templates and utilities
- **React Component Libraries** – Reusable UI components and hooks  
- **Cloud Infrastructure** – Terraform modules and Kubernetes operators
- **Developer Tools** – CLI utilities and automation scripts
- **Educational Content** – Tutorials and sample implementations

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

<h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>
{% endfor %}
{% endif %}

---

## Repository Statistics

Check out my GitHub profile for detailed statistics, contribution graphs, and pinned repositories highlighting key projects.

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
