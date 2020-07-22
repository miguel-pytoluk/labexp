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
  </style>
</head>
{% for residente in site.residentes %}
  <img class="residente-foto" src="/assets/images/residentes/{{ residente.foto }}">
  <h2>{{ residente.nome }} - {{ residente.funcao }}</h2>
  <p>{{ residente.content | markdownify }}</p>
  
{% endfor %}
