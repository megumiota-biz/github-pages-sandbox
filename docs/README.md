---
layout: default
title: "HOME"
permalink: /
nav_exclude: true
---

# Pages

{% for page in site.pages %}
{% if page.dir != "/assets/css/" %}

- {{ page.dir }}
  - [{{ page.title }}]({{ page.url | relative_url }})
    - title: {{ page.title }}
    - path: {{ page.path }}
    - name: {{ page.name }}
    - dir: {{ page.dir }}
    - permalink: {{ page.permalink }}

{% endif %}
{% endfor %}
