---
layout: home
title: "Welcome unknown..."
---

# ¡Hi! 👋

I will talk here mainly about Cybersecurity.
---

## Latest Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%d %B %Y" }}
    </li>
  {% endfor %}
</ul>

---

## About me

I am a curious person who loves to learn, write and share knowledge.  
If you want to know more, visit the page [about me](/about).

