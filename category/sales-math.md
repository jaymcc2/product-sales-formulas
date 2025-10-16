---
layout: default
title: Sales Math
permalink: /category/sales-math/
---



## Sales Math Formulas

{% assign formulas = site.data.formulas | where: "category", "sales math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
