---
layout: default
title: "Blog"
permalink: /blog/
---

# Bienvenido al blog

Reflexiones, guías y tácticas sobre **ciberseguridad**.

{% assign featured = site.posts | where_exp:"post","post.tags contains 'featured'" | first %}
{% if featured %}
<div class="featured-post">
  <h2>⭐ Post destacado</h2>
  <h3><a href="{{ featured.url | relative_url }}">{{ featured.title }}</a></h3>
  <p>{{ featured.excerpt }}</p>
</div>
{% endif %}

---

## Últimas entradas
<!-- Minima ya las lista; si tu tema no lo hace, usa este bucle -->
<ul>
  {% for post in site.posts limit:10 %}
    <li>
      <span>{{ post.date | date: "%d %b %Y" }}</span> —
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

---

## Categorías

<ul>
  {% for category in site.categories %}
    <li>
      <a href="{{ site.baseurl }}/categories/{{ category[0] | slugify }}/">
        {{ category[0] }} ({{ category[1].size }})
      </a>
    </li>
  {% endfor %}
</ul>

---

## Etiquetas

{% assign tags = site.tags | sort %}
<ul class="tag-cloud">
  {% for tag in tags %}
    <li style="font-size: {{ 0.8 | plus: tag[1].size | times: 0.1 }}rem;">
      <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}/">{{ tag[0] }}</a>
    </li>
  {% endfor %}
</ul>

---

### Sígueme

- 📡 <a href="{{ '/feed.xml' | relative_url }}">RSS</a>
- 🐦 <a href="[https://twitter.com/tuUsuario](unkwn0wn)">X/X</a>
