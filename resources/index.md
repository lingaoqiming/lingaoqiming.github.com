---
Time-stamp: <2013-07-28 23:52:14 ()>
layout: default
title: Resources
tagline: <img src="/images/pylon.png" height="30px" /> Under Construction
---

This page contains a collection of resources for a handful of
different topics. I eventually got tired of having to repeatedly track
down links and code examples for people, so I've decided to centralize
everything here.


{% for cat in site.category-list %}
### {{ cat }}
<ul>
{% for page in site.pages %}
{% if page.resource == true %}
{% for pc in page.categories %}
{% if pc == cat %}
<li>
  <a href="{{ page.url }}">{{ page.title }}</a> &mdash; {{ page.desc }}
</li>
{% endif %} <!-- cat-match-p -->
{% endfor %} <!-- page-category -->
{% endif %} <!-- resource-p -->
{% endfor %} <!-- page -->
</ul>
{% endfor %} <!-- cat -->


