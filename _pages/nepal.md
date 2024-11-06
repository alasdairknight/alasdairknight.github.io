---
layout: gallery
title: Nepal Research Trip
permalink: /nepal/
---

## Nepal Research Trip

Nepal 2024:

<div class="image-gallery">
  {% for file in site.static_files %}
    {% if file.path contains 'nepal' %}
      {% if file.extname == '.jpg' or 
        file.extname == '.jpeg' or 
        file.extname == '.JPG' or 
        file.extname == '.JPEG' %}
  
        {% assign filenameparts = file.path | split: "/" %}
        {% assign filename = filenameparts | last | replace: file.extname,"" %}
  
        <a href="{{ site.baseurl }}{{ file.path }}" title="{{ filename }}">
          <img src="{{ site.baseurl }}{{ file.path }}" alt="{{ filename }}" />
        </a>
      {% endif %}
    {% endif %}
  {% endfor %}
</div>
