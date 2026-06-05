---
layout: page
title: News
subtitle: Updates from the SLV Foundation for Education
---

<ul class="news-list">
{% for post in site.posts %}
  <li class="news-item">
    <p class="news-date">{{ post.date | date: "%B %-d, %Y" }}</p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    {% endif %}
  </li>
{% else %}
  <li class="news-item">
    <p>No news posts yet. Check back soon!</p>
  </li>
{% endfor %}
</ul>
