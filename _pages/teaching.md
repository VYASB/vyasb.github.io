---
layout: page
permalink: /teaching/
title: Teaching
description: The modules I have taught and/or assisted in class during the PhD.
years: [2023, 2022, 2021, 2020]
nav: true
nav_order: 2
---

<div class="talks">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
    {% bibliography -f teaching -q @*[year={{y}}]* %}
{% endfor %}

</div>