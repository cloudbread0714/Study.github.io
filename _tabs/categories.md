---
title: Categories
icon: fas fa-stream
order: 2
layout: categories
---
{% for cat in site.categories %}
- {{ cat[0] }} : {{ cat[1].size }} posts
{% endfor %}
