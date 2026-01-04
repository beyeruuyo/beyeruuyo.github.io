---
layout: default
title: Longreads
---

<h1>Longreads</h1>
<ul>
  {% assign pages_in_longreads = site.pages | where_exp: "item", "item.path contains 'longreads/'" %}
  {% for page in pages_in_longreads %}
    {% if page.title and page.url != '/longreads/' %}
      <li>
        <a href="{{ page.url }}">{{ page.title }}</a>
        <small>{% if page.date %}{{ page.date | date: "%d.%m.%Y" }}{% endif %}</small>
      </li>
    {% endif %}
  {% endfor %}
</ul>
