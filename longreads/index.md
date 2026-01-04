---
layout: default
title: Longreads
---

<h1>Longreads</h1>
<ul>
  {% for longread in site.longreads %}
    {% if longread.title %}
      <li>
        <a href="{{ longread.url }}">{{ longread.title }}</a>
        <small>{{ longread.date | date: "%d.%m.%Y" }}</small>
      </li>
    {% endif %}
  {% endfor %}
</ul>
