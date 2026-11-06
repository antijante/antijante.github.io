---
layout: default
title: Projects
---

# Projects

Project pages for our customers. Each one has its brief, status and anything else we share
with the customer and their team.

{% assign projects = "" | split: "" %}
{% for p in site.pages %}
  {% assign parts = p.path | split: "/" %}
  {% if parts.size == 2 and parts[1] == "index.md" %}
    {% assign projects = projects | push: p %}
  {% endif %}
{% endfor %}
{% assign projects = projects | sort: "title" %}

<ul class="project-list">
{% for p in projects %}
  <li>
    <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
    {% if p.description %}<span>{{ p.description }}</span>{% endif %}
  </li>
{% endfor %}
</ul>

Antijante builds WordPress and WooCommerce sites. More at [antijante.com](https://antijante.com).
