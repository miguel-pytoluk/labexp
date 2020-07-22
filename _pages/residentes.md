---
permalink: /residentes/
title: "Residentes"
---
<head>
  <style>
  	.residentes-container {
  	  display: flex;
  	  flex-wrap: wrap;
  	  border: 0.15em solid white;
  	  padding-top: 2.5em;
  	  margin-top: -1.5em;
  	}
  	@media only screen and (max-width: 284px) {
  	  .residentes-container {
    	    justify-content: center;
  	  }
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
	  width: 100px;
	  height: 100px;
  	  margin: 0 auto;
  	  border: 0.3em solid white;
  	}
  	.residente-dados {
  	  width:100%;
  	}
  </style>
</head>
<div class="residentes-container">
{% for residente in site.residentes %}
    <div class="residente-block">
      <img class="residente-foto" src="{{ relative_url }}assets/images/{{ residente.foto }}">
      <div class="res-foto-div"><h4 class="residente-titulo">{{ residente.nome }}</h4></div>
    </div>  
{% endfor %}
</div>
