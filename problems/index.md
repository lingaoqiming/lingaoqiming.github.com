---
Time-stamp: <2014-10-11 12:53:03 ()>
layout: default
title: Problems
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---


{% for diff in site.difficulty-levels %}
<ul>
{% for page in site.pages %}
{% if page.problem == true %}
{% if page.difficulty == diff %}
<li>
  <a href="{{ page.url }}">{{ page.title }}</a> &mdash; {{ page.desc }}
</li>
{% endif %} <!-- difficulty-match-p -->
{% endif %} <!-- problem-p -->
{% endfor %} <!-- page -->
</ul>
{% endfor %} <!-- diff -->
