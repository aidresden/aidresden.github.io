---
title: "AI Team - Baua Dresden "
layout: homelay
excerpt: "AI Team - Baua Dresden "
sitemap: false
permalink: /
---

<style>
#homepage-content {
  text-align: justify;
}
</style>

<div id="homepage-content"></div>

<!-- Load the Marked.js library from a CDN -->
<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>

<script>
document.addEventListener('DOMContentLoaded', function() {
  fetch('{{ "/assets/homepage/content.md" | relative_url }}')
    .then(response => response.text())
    .then(data => {
      // Convert Markdown text to HTML
      const htmlContent = marked.parse(data);

      // Insert rendered HTML into the page
      document.getElementById('homepage-content').innerHTML = htmlContent;
    })
    .catch(error => console.error('Error loading content:', error));
});
</script>
