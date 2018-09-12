---
layout: main
title: "A list of animals"
permalink: "/games/"
---

{% for game in site.games %}
  <div class="chapter">
    <a href="{{game.url | prepend: site.baseurl}}">
      {% if game.img %}
      <img src="{{ site.baseurl | append: "/assets/img/" | append: game.img }}" alt="{{game.title}}">
      {% endif %}
    </a>
    <div class="chapter_inner">
      <h3 class="chapter_title">{{game.title}}</h3>
    </div>
  </div>
{% endfor %}
