---
layout: page
title: Home
show_title: false
---

<section class="hero hero-grid">
  <div>
    <p class="eyebrow">Mechanical Engineering · Hardware · Software · Systems</p>

    <h1>Joseph Sciotto</h1>

    <p class="hero-subtitle">
      Mechanical engineering student at Columbia University building practical systems across
      CAD, simulation, embedded hardware, automation, and infrastructure.
    </p>

    <div class="hero-actions">
      <a class="button primary" href="/projects/">View Projects</a>
      <a class="button secondary" href="{{ '/assets/Joseph_Sciotto_Resume.pdf' | relative_url }}">View Resume</a>
      <a class="button secondary" href="/contact/">Contact</a>
    </div>
  </div>

  <img class="hero-photo" src="{{ '/assets/IMG_9227.jpg' | relative_url }}" alt="Joseph Sciotto" />
</section>

{% assign featured = site.projects | where: "featured", true | sort: "order" %}
{% if featured.size > 0 %}
<section class="section">
  <div class="section-heading">
    <h2>Featured Projects</h2>
    <p>Selected engineering, software, and infrastructure work.</p>
  </div>

  <div class="project-grid">
    {% for p in featured %}
    <article class="card project-card">
      <div>
        <p class="card-kicker">
          {% if p.stack %}{{ p.stack | join: " · " }}{% endif %}
        </p>

        <h3><a href="{{ p.url }}">{{ p.title }}</a></h3>

        {% if p.subtitle %}
        <p>{{ p.subtitle }}</p>
        {% endif %}
      </div>

      <div class="card-footer">
        {% if p.status %}<span class="pill">{{ p.status }}</span>{% endif %}
        <a href="{{ p.url }}">Read more →</a>
      </div>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}---
