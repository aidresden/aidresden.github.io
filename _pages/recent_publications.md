---
title: "Publications"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /recent_publications.html
---
<h1>Publications</h1>
<ul class="publication-list" id="publicationList">
  {% assign sorted_publications = site.publications | sort: 'date' | reverse %}
  {% assign recent_publications = sorted_publications | slice: 0, 10 %}
  {% for publication in recent_publications %}
  <li class="publication-item">
    <span class="publication-title">{{ publication.title }}</span><br>
    <span class="publication-authors">{{ publication.authors }}</span><br>
    <span class="publication-journal">{{ publication.journal }}</span>,
    <span class="publication-date">{{ publication.date | date: "%B %d, %Y" }}</span><br>
    <div class="publication-description">{{ publication.description }}</div>
    <a class="publication-link" href="{{ publication.link }}" target="_blank">Read more</a>
  </li>
  {% endfor %}
</ul>

