---
layout: page
---

{% assign rows = site.accessories.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
  <div class="row">
  {% assign offset = forloop.index0 | times: 2 %}
  {% for item in site.accessories limit:2 offset:offset %}
    <div class="col s12 m6">
      <div class="card">
        <div class="card-image">
          <img src="{{item.image}}">
        </div>
        <div class="card-content">
          <span class="card-title grey-text text-darken-4">{{item.title}}</span>
          <p>{{item.description}}</p>
        </div>
        <div class="card-action">
          <p><a href="{{site.url}}{{item.url}}">More info</a></p>
        </div>
      </div>
    </div>
  {% endfor %}
  </div>
{% endfor %}
