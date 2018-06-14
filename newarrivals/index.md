---
layout: page
---
{% assign all_products = site.accessories | concat: site.bottoms | concat: site.dresses | concat: site.tops %}
  <div class="row">
{% for product in all_products %}
  {% if product.new_arrival %}
    {% include product.html %}
  {% endif %}
{% endfor %}
  </div>
