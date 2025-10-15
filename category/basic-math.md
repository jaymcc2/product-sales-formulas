---
layout: default
title: Basic Math
permalink: /category/basic-math/
---

<h2>Basic Math Formulas</h2>
{% assign formulas = site.data.formulas | where: "category", "basic math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
