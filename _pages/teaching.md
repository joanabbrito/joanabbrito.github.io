---
layout: page
permalink: /teaching/
title: teaching
nav: true
nav_order: 6
---

{% assign courses_by_year = site.data.teaching | sort: 'year' | reverse %}
{% assign years = courses_by_year | map: 'year' | uniq %}

{% for year in years %}
<h2>{{ year }}</h2>
<ul>
  {% for course in courses_by_year %}
    {% if course.year == year %}
      <li><a href="{{ course.url }}" target="_blank">{{ course.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
{% endfor %}
