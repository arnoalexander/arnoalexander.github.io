---
layout: default
---

{% for post in site.posts %}
  <h1><a href="{{ post.url }}" style="color: inherit">{{ post.title }}</a></h1>
  <p class="meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} • {{ post.author }}{% endif %}{% if post.meta %} • {{ post.meta }}{% endif %}</p>
  <span style="text-align: justify;">{{ post.excerpt }}</span>
  <p><a href="{{ post.url }}">Read more</a></p>
  <br>
{% endfor %}