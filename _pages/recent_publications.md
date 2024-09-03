---
title: "Publications"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /recent_publications.html
---

# News

{% for article in site.data.recent_publications %}
<p>{{ article.date }} <br> {{ article.headline | markdownify}}</p>
{% endfor %}
