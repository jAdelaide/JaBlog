---
layout: default
---

# Blogs:

{% for post in site.posts %}
<li><a style="{% if page.url == post.url %}color:orange;{% endif %}" href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}

