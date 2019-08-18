---
layout: default
default_footer: true
---

<div style="padding: 0 100 0 100;">
  <h2 style="text-align: center;">Check Out Or Past Projects</h2>
  <hr>
</div>

<div class="past_projects">

<div style="align: right;">
  <div style="column-count: 3; padding: 0 auto 0 auto">

   <img src="{{ site.url }}/assets/images/Unsorted/20181210_161556.jpg" alt="" height="250px" width="250px"/>

   <img src="{{ site.url }}/assets/images/Unsorted/20190314_142645.jpg" alt="" height="250px" width="250px"/>

   <img src="{{ site.url }}/assets/images/Unsorted/20190314_142648.jpg" alt="" height="250px" width="250px"/>

  </div>
</div>

  <h3>We have completed:</h3>
  <ul class="tags">
    {% for tag in site.tags %}
      {% assign t = tag | first %}
      {% assign posts = tag | last %}
      <li><span style="color: #000f00;">{{ posts | size }}</span> {{t | downcase }} projects!</li>
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
