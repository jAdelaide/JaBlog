---
layout: home
---

# Blogs:

{% for post in site.posts %}
<li><b><a style="color:darkorchid" href="{{ post.url }}">{{ post.title }}</a></b></li>
{% endfor %}

