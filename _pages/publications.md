---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<!-- Notice Box for Group Web and Google Scholar -->
<div style="background-color: #f9f9f9; border-left: 4px solid #333; padding: 15px; margin-bottom: 30px;">
  <p style="margin-bottom: 0;">
    Note: This page is no longer being actively updated. To view my complete and most recent publications, please visit our 
    <a href="https://cosine-lab.github.io/cosinelab.org/publications/" target="_blank" style="font-weight: bold;">Research Group Website</a> or follow my profile on <a href="https://scholar.google.com/citations?user=q6_uak0AAAAJ&hl=en&oi=ao" target="_blank" style="font-weight: bold;">Google Scholar</a>.
  </p>
</div>

{% include base_path %}

{% assign sorted_publications = site.publications | sort: 'date' | reverse %}

## Journal Papers
------
{% for post in site.publications reversed %}
  {% if post.tags contains 'Journal' %}
    {% include archive-single-publications.html %}
    {% if page.authors %}
      <p><strong>Authors:</strong> {{ page.authors | markdownify }}</p>
    {% endif %}
  {% endif %}
{% endfor %}

## Conference Papers
------
{% for post in site.publications reversed %}
  {% if post.tags contains 'Conference' %}
    {% include archive-single-publications.html %}
    {% if page.authors %}
      <p><strong>Authors:</strong> {{ page.authors | markdownify }}</p>
    {% endif %}
  {% endif %}
{% endfor %}

## Conference Abstracts and Posters
------
{% for post in site.publications reversed %}
  {% if post.tags contains 'Abstract' or post.tags contains 'Poster' %}
    {% include archive-single-publications.html %}
    {% if page.authors %}
      <p><strong>Authors:</strong> {{ page.authors | markdownify }}</p>
    {% endif %}
  {% endif %}
{% endfor %}
