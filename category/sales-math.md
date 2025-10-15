---
layout: default
title: Sales Math
---

<h2>Sales Math Formulas</h2>
{% assign formulas = site.data.formulas | where: "category", "sales math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
