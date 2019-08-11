---
layout: default
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

  <ul>
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }} --- {{ post.city }}</a>
      </li>
    {% endfor %}
  </ul>

  <hr>

  {% assign cities = [] %}
  {% for post in site.posts %}

    {% assign t = tag | first %}
    {% assign posts = tag | last %}

<!--
  {{ t | downcase }}
    <ul>
      {% for post in posts %}
        {% if post.tags contains t %}
          <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
          </li>
        {% endif %}
      {% endfor %}
    </ul>
  {% endfor %}
-->

</div>
