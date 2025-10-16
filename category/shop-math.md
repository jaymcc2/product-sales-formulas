---
layout: default
title: Shop Math
permalink: /category/shop-math/
---

{% include category-links.html category="shop math" %}

## Shop Math Formulas

{% assign formulas = site.data.formulas | where: "category", "shop math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
