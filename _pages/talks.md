---
layout: page
permalink: /blogs/
title: Blogs
description: Some interesting concepts and things I got to know
years: [2024, 2023, 2022, 2021, 2020]
nav: true
nav_order: 1
---

<div class="post">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
    {% bibliography -f talks -q @*[year={{y}}]* %}
{% endfor %}

</div>