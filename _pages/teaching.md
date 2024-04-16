---
layout: page
permalink: /teaching/
title: Teaching
description: The modules I have taught during the PhD
years: [2020 - 2024]
nav: true
nav_order: 1
---

<div class="teaching">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
    {% bibliography -f teaching -q @*[year={{y}}]* %}
{% endfor %}

</div>