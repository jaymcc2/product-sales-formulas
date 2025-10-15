---
layout: default
title: Shop Math
permalink: /category/shop-math/
---

<h2>Shop Math Formulas</h2>
{% assign formulas = site.data.formulas | where: "category", "shop math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
