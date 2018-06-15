---
layout: page
---
{% assign rows = site.bottoms.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
  <div class="row">
  {% assign offset = forloop.index0 | times: 2 %}
  {% for product in site.bottoms limit:2 offset:offset %}
    {% include product.html %}
  {% endfor %}
  </div>
{% endfor %}
{% assign product_name = site.bottoms_title %}
{% include no_products.html %}
