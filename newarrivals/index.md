---
layout: page
---

{% assign rows = site.newarrivals.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
  <div class="row">
  {% assign offset = forloop.index0 | times: 2 %}
  {% for item in site.newarrivals limit:2 offset:offset %}
    <div class="col s12 m6">
      <div class="card">
        <div class="card-image">
          <img src="{{item.image}}">
        </div>
        <div class="card-content">
          <span class="card-title"><a class="grey-text text-darken-4" href="{{site.url}}{{item.url}}">{{item.title}}</span>
          <p>{{item.description}}</p>
        </div>
      </div>
    </div>
  {% endfor %}
  </div>
{% endfor %}
