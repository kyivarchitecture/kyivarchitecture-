---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
permalink: persons
---

<h1>Персоналії</h1>
<div id="container">
{% for tag in site.tags %}
{% if tag[0] contains  "_person_" %}
<div class="{{ tag[0] }}">
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] reversed | sort: "tag[1]" %}
      <li>{% include post-link.html %}</li>
    {% endfor %}
  </ul>
  </div>
  {% endif %}
{% endfor %}
</div>
{% include tag-system-cut.html %}
{% include tag-sort-abc.html %}