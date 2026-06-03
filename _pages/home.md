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


<div id="homepage-content">
    <!-- Content from the text file will be loaded here -->
</div>

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





<!--
##################################################################
<style>
    #homepage-content {
        text-align: justify;
    }
</style>

<div id="homepage-content">
    <!-- Content from the text file will be loaded here 
</div>

<script>
    // JavaScript to load text from the content.txt file
    document.addEventListener('DOMContentLoaded', function() {
        fetch('{{ "/assets/homepage/content.md" | relative_url }}')
            .then(response => response.text())
            .then(data => {
                // Access and update the content of the div with id 'homepage-content'
                document.getElementById('homepage-content').textContent = data;
            })
            .catch(error => console.error('Error loading content:', error));
    });
</script>
##############################################
