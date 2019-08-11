---
layout: default
---

<div style="padding: 0 100 0 100;">
  <h2 style="text-align: center;">Check Out Or Past Projects</h2>
  <hr>
</div>

<section>
<ul>
{% for post in site.posts %}
  <l1><a href="{{ site.url }}/{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
</section>
