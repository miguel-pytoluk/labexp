---
permalink: /residentes/
title: "Residentes"
---
<head>
  <link href="https://fonts.googleapis.com/css2?family=Domine&display=swap" rel="stylesheet">
  <style>
  	.residentes-container {
  	  border: 0.15em solid white;
	  border-top: none;
      margin-top: -0.75rem;
      margin-left: 8.8rem;
      width: 9.9rem;
      padding: 1.5em 0 1em 2.75em;
  	}
  	.residente-block {
  	  display: flex;
	  height: fit-content;
      border: 0.15rem solid white;
      border-right: 0;
      margin: 1em 0 1.5em 0.5em;
	  max-block-size: 50em;
	  background-color: white;
  	}
	.residente-info{
	  margin: -0.15rem 0 -0.15rem 0;
	  border: 0.15rem solid white;
      border-left: 0;
	  display: grid;
	  grid-template-columns: 8rem 22rem;
	}
	.res-titulo-redes-div{
      padding: 0.25em 0.75em 0.25em 0.75em;
	  display: flex;
      flex-direction: column;
      justify-content:center;
	}
  	.residente-titulo {
	  vertical-align: baseline;
	  line-height: 1.2em;
	  display: inline-block;
	  margin: 0em 0 0em 0.2em; 
  	}
  	.residente-foto {
	  height: 6.27em;
	  width: 6.27em;
  	  background-size: cover;
  	}
  	.residente-dados {
  	  width:100%;
  	}
  	a, a:visited, a:hover{
  	  color:white;
  	}
	.res-mini-bio{
	  display: flex;
      flex-direction: column;
      justify-content:center;
	  padding-right: 1.5em;
	}  
	.page__content p {
      font-family: 'Domine', serif;
      font-size: 0.6rem;
      margin-bottom: 0;
    }
	.art_mostrar_mais{
        display: none;
    }
	.texto_invisivel{
		visibility: hidden;
	}
	@media only screen and (max-width: 768px) {
	  .residentes-container {
		margin-left: 1rem;
  	  }
	  .res-mini-bio{
		display: none;
	  }
	  .residente-block {
      	background-color: unset;
  	  }
	  .residente-info{
		grid-template-columns: 8rem;
	  }
	  .art_mostrar_mais{
        display: inline-block;
      }
	  .res-mini-bio{
		padding: 0.25em 1em 0.5em 1em;
	  }  
	}
  </style>
	<script>
	function mostrarBio(id) {
		var x = document.getElementById(id);
		if (x.style.display === "block") {
		x.style.display = "none";
		} else {
			x.style.display = "block";
		}
		}
	</script>
</head>
<div class="residentes-container">
{% for residente in site.residentes %}
    <div class="residente-block">
    	<div class="residente-foto" style="background-image:url('{{ relative_url }}assets/images/{{ residente.foto }}');"><p class="texto_invisivel">img_do_artista_img_do_artista_img_do_artista</p></div>
		<div class="residente-info">
			<div class="res-titulo-redes-div">
				<h4 class="residente-titulo">{{ residente.nome }}</h4>
				<div id="redes_{{ residente.nome | remove:' ' }}" class="redes">
					{% if residente.instagram %}
					<a href="https://instagram.com/{{ residente.instagram }}"><i class="fab fa-fw fa-instagram" aria-hidden="true"></i></a>
					{% endif %}
					{% if residente.facebook %}
					<a href="https://facebook.com/{{ residente.facebook }}"><i class="fab fa-fw fa-facebook" aria-hidden="true"></i></a>
					{% endif %}
					{% if residente.twitter %}
					<a href="https://twitter.com/{{ residente.twitter }}"><i class="fab fa-fw fa-twitter" aria-hidden="true"></i></a>
					{% endif %}
					<a class="art_mostrar_mais" href="#redes_{{ residente.nome | remove:' ' }}" onclick="mostrarBio('bio_{{ residente.nome | remove:' ' }}')"><i class="fas fa-plus-circle"></i></a>
				</div>
			</div>
			<div id="bio_{{ residente.nome | remove:' ' }}" class="res-mini-bio"><p>{{ residente.content }}</p></div>
		</div>
    </div>  
{% endfor %}
</div>
