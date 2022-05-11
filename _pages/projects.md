---
title:
layout: default
permalink: /projects/
published: true
---

<div class="ProjectContainer">

	<div class="gallery">


  {% for project in site.projects %}

  {% if project.redirect %}
  <div class="projectTile" style="background-image:url({{ project.background }});background-size:cover;">
          <a href="{{ project.redirect }}" target="_blank" style="background-color: #60c17daa;">
          <span>
              <h2>{{ project.title }} - {{ project.description }}</h2>
              <br/>
              <p>{{ project.title }} - {{ project.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="projectTile" style="background-image:url({{ project.background }});background-size:cover;">
          <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ project.title }}</h2>
              <br/>
              <p>{{ project.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
