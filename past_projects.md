---
layout: default
---

<div style="padding: 0 100 0 100;">
  <h2 style="text-align: center;">Check Out Or Past Projects</h2>
  <hr>
</div>

<div class="past_projects">
  <ul>
    {% for post in site.posts %}
      {% for tag in post.tags %}
        {% assign t = tag | first %}
        <li>
          <a href="{{ post.url }}">{{ post.title }} --- {{ t }}</a>
        </li>
      {% endfor %}
    {% endfor %}
  </ul>

  <hr>

  <ul class="tags">
    {% for tag in site.tags %}
      {% if tag != 'Post Frame' %}
        {% assign t = tag | first %}
        {% assign posts = tag | last %}
        <li>We have completed {{ posts | size }} {{t | downcase | replace:" ","-" }} projects!</li>
      {% endif %}
    {% endfor %}
  </ul>

  <hr>

  <ul class="cities">
    {% for city in site.cities %}
      {% assign c = city | first %}
      {% assign posts = city | last %}
      <li>{{city | downcase | replace:" ","-" }} has {{ posts | size }} posts</li>
    {% endfor %}
  </ul>

  <hr>

  {% for tag in site.tags %}
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
