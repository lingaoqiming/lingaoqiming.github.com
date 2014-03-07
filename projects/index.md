---
Time-stamp: <2014-03-07 15:16:51 ()>
layout: default
title: "Projects"
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---

{% for page in site.pages %}
{% if page.project == true %}
- [{{ page.title }}]({{ page.url }}) -- {{ page.desc }}
{% endif %}
{% endfor %}
