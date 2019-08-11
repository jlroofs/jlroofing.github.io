---
layout: default
---

<div style="padding: 0 100 0 100;">
  <h2 style="text-align: center;">Check Out Or Past Projects</h2>
  <hr>
</div>

<section>
<ul>
{% for post in site.posts.main %}
  <l1><a href="/posts/main/{{ post.title }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
</section>
