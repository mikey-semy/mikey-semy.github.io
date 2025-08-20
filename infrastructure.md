---
title: Инфраструктура
layout: default
---
## Сервисы и доступы

| Сервис | Тип | URL | Примечание |
|--------|-----|-----|-----------|
{% for s in site.data.sites %}
| {{ s.name }} | {{ s.type }} | {% if s.url %}[{{ s.url }}]({{ s.url }}){% else %}<span class="tag">нет/приват</span>{% endif %} | {{ s.note | default: "" }} |
{% endfor %}
