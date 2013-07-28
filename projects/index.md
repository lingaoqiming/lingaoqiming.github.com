---
Time-stamp: <2013-07-28 17:26:58 ()>
layout: default
title: "Projects"
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---

{% for page in site.pages %}
{% if page.project == true %}
- [{{ page.title }}]({{ page.url }}) {{ page.description }}
{% endif %}
{% endfor %}



