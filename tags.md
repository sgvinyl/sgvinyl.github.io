---
layout: page
title: All tags
---

{% if site.tags %}
  {% for tag in site.tags %}
    <h3 id='{{ tag[0] }}'><i class="fa-solid fa-tag"></i> {{ tag[0] }}</h3>
    <ul>
      {% for post in tag[1] %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  {% endfor %}
{% else %}
  No tags yet!
{% endif %}
