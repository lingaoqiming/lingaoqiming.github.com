---
Time-stamp: <2014-03-07 15:11:42 ()>
layout: default
title: "Projects"
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---

{% for page in site.pages %}
{% if page.project == true %}
- [{{ page.title }}]({{ page.url }}) {{ page.description }}
{% endif %}
{% endfor %}
