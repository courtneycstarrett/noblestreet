---
layout: page
---
{% assign rows = site.tops.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
  <div class="row">
  {% assign offset = forloop.index0 | times: 2 %}
  {% for product in site.tops limit:2 offset:offset %}
    {% include product.html %}
  {% endfor %}
  </div>
{% endfor %}
