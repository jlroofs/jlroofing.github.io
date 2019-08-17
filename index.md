---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
default_footer: true
---
<h3>Check out our latest project!</h3>
{% for post in site.posts limit:1 %}
  {{ post }}
{% endfor %}
