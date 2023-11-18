---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
permalink: locations
---

<h1>Райони</h1>

{% for tag in site.tags | sort: "address_no" %}
{% if tag[0] contains  "_loc_" %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
    
      <li>{% include post-link.html %}</li>
    {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

{% include tag-system-cut.html %}