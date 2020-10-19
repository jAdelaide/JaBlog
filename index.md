---
layout: home
---

# Blogs:

{% for post in site.posts %}
<li><a style="{% if page.url == post.url %}color:orange;{% endif %}" href="/-JaBlog-{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}

