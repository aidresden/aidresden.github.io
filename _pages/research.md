---
title: "AI Team - Baua Dresden "
layout: textlay
excerpt: "AI Team - Baua Dresden "
sitemap: false
permalink: /research/
---

# Research Overview
{% assign research_data = site.data.research_overview %}

<p>{{ research_data.overview_description }}</p>

### Ongoing Research Projects
{% for project in research_data.ongoing_projects %}
  <h5><strong>{{ project.title }}</strong></h5> <!-- Make title bold -->
  <img src="{{ project.image }}" alt="{{ project.title }}" style="max-width:100%; height:auto;"> <!-- Display image -->
  <p>{{ project.description }}</p>
  <a href="{{ project.link }}">Learn more about {{ project.title }}</a>
{% endfor %}

### Finished Research Projects
{% for project in research_data.finished_projects %}
  <h5><strong>{{ project.title }}</strong></h5> <!-- Make title bold -->
  <img src="{{ project.image }}" alt="{{ project.title }}" style="max-width:100%; height:auto;"> <!-- Display image -->
  <p>{{ project.description }}</p>
  <a href="{{ project.link }}">Learn more about {{ project.title }}</a>
{% endfor %}
