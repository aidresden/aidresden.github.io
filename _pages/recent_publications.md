---
title: "Recent Publications"
layout: textlay
excerpt: "BAuA AI Team Recent Publications"
sitemap: false
permalink: /recent_publications.html
---
<h1>Publications</h1>
<ul class="publication-list" id="publicationList">
  {% assign sorted_publications = site.publications | sort: 'date' | reverse %}
  {% assign recent_publications = sorted_publications | slice: 0, 10 %}
  {% for publication in recent_publications %}
  <li class="publication-item">
    <span class="publication-title" style="font-weight: bold;">{{ publication.title }}</span><br>
    <span class="publication-authors" style="font-style: italic;">{{ publication.authors }}</span><br>
    <span class="publication-journal">{{ publication.journal }}</span>,
    <span class="publication-date" style="font-size: 0.875em;">{{ publication.date | date: "%B %d, %Y" }}</span><br>
    <div class="publication-description">{{ publication.description }}</div>
    <a class="publication-link" href="{{ publication.link }}" target="_blank">Read more</a>
  </li>
  {% endfor %}
</ul>
