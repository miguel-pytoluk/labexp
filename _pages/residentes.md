---
permalink: /residentes/
title: "Residentes"
---
<head>
  <style>
  	.residente-foto {
  	  border-radius: 50%;
  	  object-fit: cover;
	  width: 200px;
	  height: 200px;
  	}
  	.residente-block {
  	  display: inline-block;
  	}
  </style>
</head>
{% for residente in site.residentes %}
  <div class="residente-block">
    <img class="residente-foto" src="{{ relative_url }}assets/images/{{ residente.foto }}">
  </div>
  <div class="residente-block">
    <h2>{{ residente.nome }} - {{ residente.funcao }}</h2>
    <p>{{ residente.content | markdownify }}</p>
  </div>
  
{% endfor %}
