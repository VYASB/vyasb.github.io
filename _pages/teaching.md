---
layout: page
permalink: /teaching/
title: Teaching
description: During my PhD, I have performed demonstrator duties for the practical lab of following modules.
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