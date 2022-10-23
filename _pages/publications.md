---
layout: page
permalink: /publications/
title: publications
types: [journal, conference, tutorial, workshop, abstract,  preprint, thesis]
# years: [2022, 2021, 2020, 2019, 2018]
nav: true
nav_order: 1
---

<div class="publications">

{% for t in page.types %}
  <h2 class="year">{{t}}</h2>
  {% bibliography -f papers -q @*[keywords={{t}}]* %} 
{% endfor %}

</div>








