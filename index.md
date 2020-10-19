---
layout: home
---

# Blogs:

{% for post in site.posts %}
<li><a style="color:darkorchid" href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}

