---
title: Проекты
layout: src/_includes/base.njk
---
## Проекты

{% set projects = collections.frontMatterProjects or require('./_data/projects.json') %}

<table>
<tr><th>Проект</th><th>Описание</th><th>Ссылка</th></tr>
{% for p in projects %}
<tr>
  <td>{{ p.name }}</td>
  <td>{{ p.description }}</td>
  <td>
    {% if p.url %}<a href="{{ p.url }}" target="_blank">{{ p.url }}</a>{% else %}<span class="tag">приватный</span>{% endif %}
  </td>
</tr>
{% endfor %}
</table>
