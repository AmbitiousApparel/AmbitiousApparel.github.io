---
title: Purchase Links
layout: default
---

<div align="center">
	<h1>Purchase Links</h1>
</div>

{% for link in site.data.linkList %}
  {% if link.break %}
  <div class="jumbotron">
  <h2 class="no-border">{{link.name}}</h2>
  </div>
  {% else %}
    {% if link.hasLink %}
  <h3><a href="{{link.link}}" target="_blank">{{link.name}}</a></h3>
    {% else %}
  <h3>{{link.name}}</h3>
    {% endif %}

  <div class="container-fluid">
    <div class="col-md-4">
      <p>{{link.description}}</p>
    </div>
    <div class="col-md-8">
    </div>
  </div>
  		
  {% endif %}
{% endfor %}
