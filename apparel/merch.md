---
title: Apparel
layout: default
---

<div align="center">
	<h1>Apparel</h1>
</div>

{% for merch in site.data.merchList %}
  {% if merch.break %}
  <div class="jumbotron">
  <h2 class="no-border">{{merch.name}}</h2>
  </div>
  {% else %}
    {% if merch.hasLink %}
  <h3><a href="{{merch.link}}" target="_blank">{{merch.name}}</a></h3>
    {% else %}
  <h3>{{merch.name}}</h3>
    {% endif %}

  <div class="container-fluid">
    <div class="col-md-4">
      <p>{{merch.description}}</p>
    </div>
    <div class="col-md-8">
    {% if merch.image %}
      <img class="img-responsive" src="{{merch.image}}" alt="{{merch.image}}">
    {% endif %}
    </div>
  </div>
  		
  {% endif %}
{% endfor %}
