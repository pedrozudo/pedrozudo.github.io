---
layout: page
permalink: /publications/
title: publications
types: [journal, conference, tutorial, workshop, abstract,  preprint, thesis]
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018]
months: [12,11,10,9,8,7,6,5,4,3,2,1]
nav: true
nav_order: 1
---

<div class="publications">

{% for t in page.types %}
<h2 class="year">{{t}}</h2>
  {% for y in page.years %}
    {% for m in page.months %}
      {% bibliography -f papers -q @*[keywords={{t}},year={{y}},num_month={{m}}]* %}
    {% endfor %}
  {% endfor %}
{% endfor %}

</div>
