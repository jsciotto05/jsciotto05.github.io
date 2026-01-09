---
layout: page
title: Projects
permalink: /projects/
---

These are deep dives into what I built, why I built it, the tradeoffs, and what I’d improve.

## Curated write-ups
{% assign sorted = site.projects | sort: "order" %}
{% for p in sorted %}
<div class="card">
  <h2><a href="{{ p.url }}">{{ p.title }}</a></h2>
  {% if p.subtitle %}<p class="subtitle">{{ p.subtitle }}</p>{% endif %}
  <p class="meta">
    {% if p.stack %}Stack: {{ p.stack | join: ", " }}{% endif %}
    {% if p.status %}<span class="pill">{{ p.status }}</span>{% endif %}
  </p>
  {% if p.summary %}<p>{{ p.summary }}</p>{% endif %}
</div>
{% endfor %}

---

## All GitHub repos (auto)
<div id="repo-list"></div>

<script>
(async function () {
  const user = "jsciotto05";
  const res = await fetch(`https://api.github.com/users/${user}/repos?per_page=100&sort=updated`);
  const repos = await res.json();

  const container = document.getElementById("repo-list");
  container.innerHTML = repos
    .filter(r => !r.fork)
    .map(r => `
      <div class="card">
        <h3><a href="${r.html_url}">${r.name}</a></h3>
        <p class="meta">Updated: ${new Date(r.updated_at).toLocaleDateString()} · ${r.language ?? ""} · ⭐ ${r.stargazers_count}</p>
        <p>${r.description ?? ""}</p>
      </div>
    `)
    .join("");
})();
</script>
