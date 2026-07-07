---
layout: default
title: Projects
---

# Projects

<div class="project-grid">
  {% for project in site.projects %}
    <div class="project-card">
      {% if project.thumbnail %}
        <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }}">
      {% endif %}
      <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
      <p>{{ project.description }}</p>
      {% if project.tech %}
        <ul class="tech-list">
          {% for t in project.tech %}<li>{{ t }}</li>{% endfor %}
        </ul>
      {% endif %}
    </div>
  {% endfor %}
</div>