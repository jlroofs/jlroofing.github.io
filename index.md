---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
default_footer: true
---
<h3 id="main_page">Check out our latest project!</h3>
{% for post in site.posts limit:1 %}
  {{ post.excerpt }}
  {% include cc_copyright_notice.html %}
{% endfor %}

{% for post in posts %}
  {% for image in post.images %}
    <div class="lightbox" id="lightbox{{ forloop.index }}">
      <div class="table">
        <div class="table-cell">
          <img class="close" src="/img/close.svg" />
          <img class="next" src="/img/next.svg" />
          <img class="prev" src="/img/prev.svg" />
          <div class="item" style="background: url('{{ item.image }}') center center no-repeat; background-size: cover;">
          </div>
        </div>
      </div>
    </div>
{% endfor %}

$('.next').click(function(){
  $(this).closest('.lightbox').hide().next().show();
});
