---
title: Проекты
layout: default
---
## Проекты

| Проект | Описание | Ссылка |
|--------|----------|--------|
{% for p in site.data.projects %}
| {{ p.name }} | {{ p.description }} | {% if p.url %}[{{ p.url }}]({{ p.url }}){% else %}<span class="tag">приватный</span>{% endif %} |
{% endfor %}
