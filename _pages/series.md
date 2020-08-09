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
      font-weight: bold;
    }
    .cascata, .fa-angle-down{
      position: absolute;
      display:none;
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
      max-width: 10.16em;
    }
    .series-navitem{
      margin-top: 1em;
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
    @media only screen and (max-width: 768px) {
      .tit_serie_principal {
        margin-left: 0;
        margin-right: 0;
      }
      .fa-angle-down{
        display: block;
        margin-left: -0.45em;
        margin-top: 0.45em;
      }
      .cascata {
        position: absolute;
        display: block;
      }
      .serie_principal_div_vazia{
        display: none;
      }
      .serie_principal_titulo{
        border-left: 0.1em solid white;
        margin-left: 0.75em;
      }
      .nav_e_video_serie{
        margin-left: 0.1em;
      }
      .serie_nav{
        background-color: #141010;
        display:none;
        position: absolute;
        z-index: 1;
        margin: 0;
      }
      .video-container{
        margin-left: 0;
        margin-right: 0;
      }
      .texto-serie{
        margin: 0;
        margin-left: 0;
        margin-right: 0;
        padding-top: 1em;
        padding-bottom: 1em;
      }
      .artistas_presentes{
        padding-top: .75em;
        padding-bottom: 1em;
      }
      .artistas_serie{
        margin: 2em 0 0 0;
      }
      .nav_e_video_serie, .artistas_serie{
        grid-template-columns: auto;
      }
      .artistas_fotos_e_lista{
        padding: 1em 0 0 0;
      }
      .art_foto_div a h5{
        font-size: 0.7rem;
      }
      .artistas_lista a h5{
        font-size: 0.6rem;
      }
      .artistas_fotos{
        grid-template-columns: 29.5% 29.5% 29.5%;
        column-gap: 1em;
      }
      .artista_foto{
        height: 3em;
        width: 100%;
      }
    }
  </style>
  <script>
    function mostrarNav() {
      var x = document.getElementById("serie_nav");
      if (x.style.display === "block") {
        x.style.display = "none";
      } else {
          x.style.display = "block";
          x.style.marginLeft = "-0.1em";
      }
     }
  </script>
</head>
<div class="tit_serie_principal">
  <a class="cascata" href="javascript:void(0);" onclick="mostrarNav()"><i class="fa fa-angle-down" aria-hidden="true"></i></a>
  <div class="serie_principal_div_vazia"></div>
  <div class="serie_principal_titulo">_Sessões Tronco</div>
</div>
<div class="nav_e_video_serie">
  <nav class="serie_nav" id="serie_nav">
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
