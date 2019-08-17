---
layout: default
default_footer: true
---

<div style="padding: 0 100 0 100;">
  <h2 style="text-align: center;">Check Out Or Past Projects</h2>
  <hr>
</div>

<div class="past_projects">

  <h3>We have completed:</h3>
  <ul class="tags">
    {% for tag in site.tags %}
      {% assign t = tag | first %}
      {% assign posts = tag | last %}
      <li>{{ posts | size }} {{t | downcase }} projects!</li>
    {% endfor %}
  </ul>

  <hr>

  <ul style="column-count: 3">
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }} --- {{ post.city }}</a>
      </li>
    {% endfor %}
  </ul>

</div>
