---
Time-stamp: <2014-10-11 12:48:10 ()>
layout: default
title: Problems
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---


{% for difficulty in site.difficulty-levels %}
<ul>
{% for page in site.pages %}
{% if page.problem == true %}
{% if page.difficulty == difficulty %}
<li>
  <a href="{{ page.url }}">{{ page.title }}</a> &mdash; {{ page.desc }}
</li>
{% endif %} <!-- difficulty-match-p -->
{% endif %} <!-- problem-p -->
{% endfor %} <!-- page -->
</ul>
{% endfor %} <!-- difficulty -->
