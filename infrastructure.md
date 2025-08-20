---
title: Инфраструктура
layout: src/_includes/base.njk
---
## Сервисы и доступы

{% set sites = require('./_data/sites.json') %}

<table>
<tr><th>Сервис</th><th>Тип</th><th>URL</th><th>Примечание</th></tr>
{% for s in sites %}
<tr>
  <td>{{ s.name }}</td>
  <td>{{ s.type }}</td>
  <td>
    {% if s.url %}<a href="{{ s.url }}" target="_blank">{{ s.url }}</a>{% else %}<span class="tag">нет/приват</span>{% endif %}
  </td>
  <td>{{ s.note or "" }}</td>
</tr>
{% endfor %}
</table>
