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

  <h2 class="mt-4">{{ year }}</h2>
  <div class="row row-cols-1 row-cols-md-3">
    {% for course in courses_by_year %}
      {% if course.year == year %}
        <div class="col mb-4">
          <a href="{{ course.url }}" target="_blank" style="text-decoration: none; color: inherit;">
            <div class="card h-100 hoverable">
              <div class="card-body">
                <h5 class="card-title">{{ course.title }}</h5>
                <p class="card-text text-muted">Instituto Superior Técnico, ULisboa</p>
              </div>
            </div>
          </a>
        </div>
      {% endif %}
    {% endfor %}
  </div>
{% endfor %}
