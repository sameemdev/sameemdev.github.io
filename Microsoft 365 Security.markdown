---
layout: page
title: Microsoft 365 Security
permalink: /basic-cybersecurity/
---

<ul>
  {% for post in site.categories.m365 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span> — {{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
