---
layout: page
permalink: /publications/
title: Publications
description:
years: [2015, 2017, 2018, 2020]
nav: true
---

<div class="publications">

{% assign years_sorted = page.years | sort | reverse %}
{% for y in years_sorted %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
