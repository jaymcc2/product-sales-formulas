---
layout: default
title: Basic Math
permalink: /category/basic-math/
---

{% include category-links.html category="basic math" %}

## Basic Math

{% assign formulas = site.data.formulas | where: "category", "basic math" %}
{% for formula in formulas %}
  {% include formula.html formula=formula %}
{% endfor %}
