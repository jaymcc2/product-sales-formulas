---
layout: default
title: Shop Math
---

<h2>Shop Math Formulas</h2>
{% assign formulas = site.data.formulas | where: "category", "shop math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
