---
layout: default
title: Sales Math
permalink: /category/sales-math/
---

<h2>Sales Math Formulas</h2>
{% assign formulas = site.data.formulas | where: "category", "sales math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
