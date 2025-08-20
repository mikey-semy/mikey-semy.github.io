---
title: Проекты
layout: default
---

## Проекты

<table>
  <thead>
    <tr><th>Проект</th><th>Описание</th><th>Ссылка</th></tr>
  </thead>
  <tbody>
  {% for p in site.data.projects %}
    <tr>
      <td>{{ p.name }}</td>
      <td>{{ p.description }}</td>
      <td>
        {% if p.url %}
          <a href="{{ p.url }}" target="_blank" rel="noopener">{{ p.url }}</a>
        {% else %}
          <span class="tag">приватный</span>
        {% endif %}
      </td>
    </tr>
  {% endfor %}
  </tbody>
</table>
