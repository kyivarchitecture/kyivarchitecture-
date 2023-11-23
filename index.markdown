---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
permalink: /
---

<ul>
  {% for post in site.posts reversed %}
    <li>
      {% include post-link.html %}
    </li>
  {% endfor %}
</ul>
