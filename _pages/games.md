---
layout: main
title: "A list of animals"
permalink: "/games/"
---

{% for game in site.games %}
  <div class="chapter">
      {% if game.img %}
      ![{{game.title}}]({{ site.baseurl | append: /assets/img/ | append: game.img }})
      {% endif %}
    <div class="chapter_inner">
      <h3 class="chapter_title">{{game.title}}</h3>
    </div>
  </div>
{% endfor %}
