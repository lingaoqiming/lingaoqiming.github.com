---
Time-stamp: <2013-07-27 19:57:23 ()>
layout: default
title: "Projects"
---

{% for page in site.pages %}
{% if page.project == true %}
- [{{ page.title }}]({{ page.url }}) {{ page.description }}
{% endif %}
{% endfor %}



