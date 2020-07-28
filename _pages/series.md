---
permalink: /series/
title: "Séries"
---
<head>
  <link href="https://fonts.googleapis.com/css2?family=Domine&display=swap" rel="stylesheet">
  <style>
    .tit_serie_principal {
      display: grid;
      padding-left: 1em;
      grid-template-columns: 10.16em auto;
      border: 0.1em solid white;
    }
    .serie_principal_div_vazia{
      border: 0.1em solid white;
      border-top: 0;
      border-bottom: 0;
      padding-top: 0.25em;
    }
    .serie_principal_titulo{
      padding-top: 0.25em;
      padding-left: 1em;
    }
    .nav_e_video_serie, .artistas_serie{
      display: grid;
      margin-left: 1.1em;
      grid-template-columns: 10.16em auto;
    }
    .serie_nav{
      padding-left: 1em;
      border: 0.1em solid white;
      border-top: 0;
      min-height: 11em;
    }
    .series-navitem{
      margin-top: 1em;
    }
    .series-navitem a {
      font-weight: bold;
    }
    a, a:visited, a:hover{
      color:white;
    }
    .video-container{
      padding-bottom: 0.1em;
    }
    .texto-serie{
      margin-top: -0.1em;
      margin-left: 11.15em;
      padding: 1.5em 1em;
      border: 0.1em solid white;
    }
    .page__content p {
      font-family: 'Domine', serif;
      font-size: 0.6rem;
      margin-bottom: 0;
    }
    .artistas_serie{
      margin-top: -0.05em;
    }
    .artistas_presentes{
      border: 0.1em solid white;
      padding: 1.5em 1em 2em 1em;
      height: min-content;
    }
    .artistas_presentes h1{
      margin-bottom: 0;
    }
    .artistas_fotos_e_lista{
      padding: 2em 2.5em;
    }
    .artistas_fotos{
      display: grid;
      grid-template-columns: auto auto auto;
      column-gap: 1.5em;
    }
    .artista_foto{
      border: 0.1em solid white;
      background-color: white;
      height: 6em;
      width: 100%;
      object-fit: cover;
    }
    .art_foto_div h5 {
      margin-top: 0.2em;
      margin-bottom: 1em;
    }
    .artistas_lista{
      display: grid;
      grid-template-columns: repeat(4, minmax(auto, auto));
      justify-content: space-between;
    }
    .artistas_lista h5{
      margin-top: 0.2em;
      margin-bottom: 0.2em;
    }
    .artistas_lista a, .art_foto_div a{
      text-decoration: none;
    }
  </style>
</head>
<div class="tit_serie_principal">
  <div class="serie_principal_div_vazia"></div>
  <div class="serie_principal_titulo">_Sessões Tronco</div>
</div>
<div class="nav_e_video_serie">
  <nav class="serie_nav">
    <ul>
      <li class="series-navitem"><a href="#">_Outra série</a></li>
      <li class="series-navitem"><a href="#">_Mais uma série</a></li>
      <li class="series-navitem"><a href="#">_Uma Série com o Nome Maior</a></li>
    </ul>
  </nav>
  <div class="video-container">
    <iframe class="series-video" width="560" height="315" src="https://www.youtube.com/embed/videoseries?list=PLDXfT5I07qSI7DlWwRu_0v8Po0Icw0HI8&autoplay=1&mute=1" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>
<div class="texto-serie">
  <p>Texto sobre as Sessões Tronco landit hendrerit. Aenean sit amet nisi. Nec orci ornare consequat. 
Praesent lacinia ultrices consectetur. Sed non ipsum felis. Quem num gosta di mim que vai caçá sua turmis! Nullam volutpat risus nc leo commodo, ut interdum diam laoreet. Sed non consequat odio. 
Si u mundo tá muito paradis? Toma um</p>
</div>
<div class="artistas_serie">
  <div class="artistas_presentes">
    <h1>Artistas presentes nas Séries_lab</h1>
  </div>
  <div class="artistas_fotos_e_lista">
    <div class="artistas_fotos">
    {% for artista_full in site.artistas limit:3 %}
      <div class="art_foto_div">
        <img class="artista_foto" src="/LabXP/artistas/assets/images/{{ artista_full.foto }}">
        <a href="#"><h5>_{{ artista_full.nome }}</h5></a>
      </div>
    {% endfor %}
    </div>
    <div class="artistas_lista">
      {% for artista in site.artistas offset:4 limit:4 %}
      <a href="#"><h5>_{{ artista.nome }}</h5></a>
      {% endfor %}
    </div>
    <div class="artistas_lista">
      {% for artista in site.artistas offset:8 limit:4 %}
      <a href="#"><h5>_{{ artista.nome }}</h5></a>
      {% endfor %}
    </div>
    <div class="artistas_lista">
      {% for artista in site.artistas offset:12 limit:4 %}
      <a href="#"><h5>_{{ artista.nome }}</h5></a>
      {% endfor %}
    </div>
    <div class="artistas_lista">
      {% for artista in site.artistas offset:16 limit:4 %}
      <a href="#"><h5>_{{ artista.nome }}</h5></a>
      {% endfor %}
    </div>
    <div class="artistas_lista">
      {% for artista in site.artistas offset:20 limit:4 %}
      <a href="#"><h5>_{{ artista.nome }}</h5></a>
      {% endfor %}
    </div>
    <div class="artistas_lista">
      {% for artista in site.artistas offset:24 limit:4 %}
      <a href="#"><h5>_{{ artista.nome }}</h5></a>
      {% endfor %}
    </div>
  </div>
</div>
