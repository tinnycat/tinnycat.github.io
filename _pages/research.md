---
title:
layout: default
permalink: /research/
published: true
---


<div class="researchContainer">

  <div class="gallery">


    {% for research in site.research %}

    {% if research.redirect %}
    <div class="researchTile">
      <a href="{{ research.redirect }}" target="_blank">
        <span>
          <h2>{{ research.title }}</h2>
          <br />
          <p>{{ research.description }}</p>
        </span>
      </a>
    </div>

    {% else %}

    <div class="researchTile">
      <a href="{{ research.url | prepend: site.baseurl | prepend: site.url }}">
        <span>
          <h2>{{ research.title }}</h2>
          <br />
          <p>{{ research.description }}</p>
        </span>
      </a>
    </div>

    {% endif %}

    {% endfor %}

  </div>

</div>