---
layout: page
title: Home
---

# Joseph Sciotto
I build engineering systems across hardware + software: simulations, tools, embedded-ish projects, and infrastructure.

- GitHub: https://github.com/jsciotto05
- Projects: /projects/
- Resume: /resume/

## Featured Projects
{% assign featured = site.projects | where: "featured", true %}
{% for p in featured %}
<div class="card">
  <h2><a href="{{ p.url }}">{{ p.title }}</a></h2>
  {% if p.subtitle %}<p class="subtitle">{{ p.subtitle }}</p>{% endif %}
  <p class="meta">
    {% if p.stack %}Stack: {{ p.stack | join: ", " }}{% endif %}
    {% if p.status %}<span class="pill">{{ p.status }}</span>{% endif %}
  </p>
</div>
{% endfor %}
