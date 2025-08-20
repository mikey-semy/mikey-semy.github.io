---
title: Инфраструктура
layout: default
---

## Сервисы и доступы

<table>
  <thead>
    <tr><th>Сервис</th><th>Тип</th><th>URL</th><th>Примечание</th></tr>
  </thead>
  <tbody>
  {% for s in site.data.sites %}
    <tr>
      <td>{{ s.name }}</td>
      <td>{{ s.type }}</td>
      <td>
        {% if s.url %}
          <a href="{{ s.url }}" target="_blank" rel="noopener">{{ s.url }}</a>
        {% else %}
          <span class="tag">нет/приват</span>
        {% endif %}
      </td>
      <td>{{ s.note | default: "" }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
