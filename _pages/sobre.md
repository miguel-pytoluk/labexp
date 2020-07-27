---
permalink: /sobre/
title: "Sobre"
---
<head>
  <link href="https://fonts.googleapis.com/css2?family=Domine&display=swap" rel="stylesheet">
  <style>
    h3 {
      margin-top: 0em;
    }
    #sobre_1o_card{
      width: 17.3em;
      border: 0.1em solid white;
      border-top: 0;
      padding: 1em;
      margin-left: 1.55em;
      padding-bottom: 0.1em;
    }
    .page__content p {
      font-family: 'Domine', serif;
      font-size: 0.6rem;
    }
    #sobre_2o_card{
      border: 0.1em solid white;
      margin-top: -0.1em;
      margin-left: 18.75em;
      height: 14em;
      width: 22.95em;
      background-color: white;
    }
    #sobre_2o_card img{
      height: 13.8em;
      width: 22.75em;
      object-fit: cover;
      margin-left: 0.01em;
      background-color: white;
    }
    #sobre_3o_card{
      border: 0.1em solid white;
      margin-top: -0.1em;
      margin-left: 10.85em;
      width: 8em;
      padding: 1.5em 0 1em 2em;
    }
    #sobre_3o_card h1 {
      margin-bottom: 0em;
    }
    .mente-block {
      display: flex;
      border: 0.1em solid white;
      border-right: 0;
      margin: 1em 0 1.5em 0.5em;
      background-color: white;
    }
    .mente-foto{
      height: 5.066em;
      background-color: white;
    }
    .men-titulo-div, .redes{
      border: 0.1em solid white;
      border-left: 0;
      margin: -0.1em 0 -0.1em 0.1em;
      padding-top: 0.1em;
      padding-bottom: 0.1em;
    }
    .men-titulo-div{
      padding-left: 1em;
      margin-right: 0;
      border-right: 0;
    }
    .men-titulo-div h4, .men-titulo-div h5{
      width: 9em;
    }
    .page__content h6 {
      margin: 0 0 0 0;
      font-family: 'Domine', serif;
      font-size: 0.6rem;
      font-weight: normal;
    }
    .mente-nome{
      margin: 0.5em 0 0.25em 0; 
    }
    .redes{
      margin-left: -0.007em;
      padding-right: 0.2em;
    }
    a, a:visited, a:hover{
  	  color:white;
    }
    @media only screen and (max-width: 768px) {
    	#sobre_1o_card{
	      width: 100%;
	      margin-left: 0;
	    }
	    #sobre_2o_card{
	      margin: auto;
	      width: 100%;
	    }
	    #sobre_2o_card img{
	      width: 100%;
	    }
	    #sobre_3o_card{
	      margin-left: 0em;
	    }
	}
  </style>
</head>

<div id="sobre_1o_card">
  <h3>Somos um lugar lindo maravilhoso venha você tbm tá ligado, agora ou nunca.</h3>

  <p class="sobre-paragrafo">O lab_xp foi criado para isso e isso mussum Ipsum, tempor enim ad qui ullamco. Est dolore anim ad velit duis dolore minim sunt aliquip amet commodo labore. Ut eu pariatur aute ea aute excepteur laborum. Esse ea esse excepteur minim mollit qui cillum excepteur ex dolore magna. Labore deserunt fugiat incididunt incididunt sint ea. Consequat dolore aute laboris quis proident quis non et est consectetur ex eiusmod sit culpa.</p>

  <p class="sobre-paragrafo">Cupidatat ea do et in excepteur in. Ad nostrud ut est esse eu duis ea sunt eiusmod. Aliquip tempor veniam sint elit fugiat. Velit incididunt laboris amet incididunt labore dolore irure velit excepteur commodo deserunt laborum. Consectetur eu fugiat veniam veniam Lorem labore magna eiusmod. Ea occaecat reprehenderit pariatur consectetur minim labore ut aliquip. </p>
</div>
<div id="sobre_2o_card">
  <img src="/LabXP/assets/images/sobrelabxp.jpg" alt="um dia de LabXP">
</div>
<div id="sobre_3o_card">
  <h1>LabXP</h1>
  <h1>é</h1>
  {% for mente in site.sobre %}
    <div class="mente-block">
      <img class="mente-foto" src="{{ relative_url }}assets/images/{{ mente.foto }}">
      <div class="men-titulo-div">
        <h4 class="mente-nome">{{ mente.nome }}</h4>
        <h6 class="mente-funcao">{{ mente.funcao }}</h6>
        {% if mente.funcao2 %}<h6 class="mente-funcao2">{{ mente.funcao2 }}</h6>{% endif %}
      </div>
      <div class="redes">
      	{% if mente.instagram %}
      	<a href="https://instagram.com/{{ mente.instagram }}"><i class="fab fa-fw fa-instagram" aria-hidden="true"></i></a>
      	{% endif %}
      	{% if mente.facebook %}
      	<a href="https://facebook.com/{{ mente.facebook }}"><i class="fab fa-fw fa-facebook" aria-hidden="true"></i></a>
      	{% endif %}
      	{% if mente.twitter %}
      	<a href="https://twitter.com/{{ mente.twitter }}"><i class="fab fa-fw fa-twitter" aria-hidden="true"></i></a>
      	{% endif %}
      </div>
    </div>  
  {% endfor %}
</div>
