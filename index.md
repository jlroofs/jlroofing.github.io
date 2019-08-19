---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
default_footer: true
under_construction: true
---
<h2>JLRoofing</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
<hr>
<h3 id="main_page">Check out our latest project!</h3>
{% for post in site.posts limit:1 %}
  {{ post.excerpt }}
  {% include cc_copyright_notice.html %}
{% endfor %}

<!--
$('.next').click(function(){
  $(this).closest('.lightbox').hide().next().show();
});
-->
