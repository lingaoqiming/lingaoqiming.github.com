---
Time-stamp: <2014-10-11 12:59:03 ()>
layout: default
title: Problems
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---

This page contains a collection of programming problems. Being able to
solve these problems proficiently is a good start if you are planning
on applying for an internship or full time position at a tech company.

{% for diff in site.difficulty-levels %}
### {{ diff }}
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
