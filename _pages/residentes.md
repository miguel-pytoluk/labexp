---
permalink: /residentes/
title: "Residentes"
---
<head>
  <style>
  	.residentes-container {
  	  display: grid; /* 1 */
  	  grid-template-columns: repeat(auto-fill, 130px); /* 2 */
  	  grid-gap: 1rem; /* 3 */
  	  justify-content: space-evenly; /* 4 */
  	  border: 0.15em solid white;
  	  padding-top: 2.5em;
  	  margin-top: -1.5em;
  	}
  	.residente-block {
  	  display: inline-block;
  	  margin: 0 0.75em;
  	}
	.res-foto-div{
	  display: flex;
    	  justify-content: center;
	}
  	.residente-titulo {
  	  text-align: center;
  	  margin-top: 0.5em;
  	  width: 100px;
  	}
  	.residente-foto {
  	  display: block;
  	  object-fit: cover;
	  height: 100px;
	  width: 100px;
  	  margin: 0 auto;
  	  border: 0.3em solid white;
  	  background-color: white;
  	}
  	.residente-dados {
  	  width:100%;
  	}
  	a, a:visited{
  	  color:white;
  	}
  </style>
</head>
<div class="residentes-container">
{% for residente in site.residentes %}
    <div class="residente-block">
      <img class="residente-foto" src="{{ relative_url }}assets/images/{{ residente.foto }}">
      <div class="res-foto-div"><h4 class="residente-titulo">{{ residente.nome }}</h4></div>
      <div class="redes">
      	{% if residente.instagram %}
      	<a href="https://instagram.com/{{ residente.instagram }}"><i class="fab fa-fw fa-instagram" aria-hidden="true"></i></a>
      	{% endif %}
      	{% if residente.facebook %}
      	<a href="https://facebook.com/{{ residente.facebook }}"><i class="fab fa-fw fa-facebook" aria-hidden="true"></i></a>
      	{% endif %}
      </div>
    </div>  
{% endfor %}
</div>
