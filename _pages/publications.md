---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% assign sorted_publications = site.publications | sort: 'date' | reverse %}

## Journal Papers
------
{% for post in site.publications reversed %}
  {% if post.tags contains 'journal' %}
    {% include archive-single.html %}
    {% if page.authors %}
      <p><strong>Authors:</strong> {{ page.authors | markdownify }}</p>
    {% endif %}
  {% endif %}
{% endfor %}

## Conference Papers
------
{% for post in site.publications reversed %}
  {% if post.tags contains 'conference' %}
    {% include archive-single.html %}
    {% if page.authors %}
      <p><strong>Authors:</strong> {{ page.authors | markdownify }}</p>
    {% endif %}
  {% endif %}
{% endfor %}
