<script setup>
import BaseHeader from '../components/BaseHeader.vue'
import BaseFooter from '../components/BaseFooter.vue'
</script>

<template>

	<BaseHeader />

  <main>
		<img src="../assets/Logotix-Bluetext.png" width="150px">

    <h1>Stan Robotix</h1>
    <p>Petit paragraphe d'accueil. Lorem ipsum dolor sit amet,
      consectetur adipiscing elit, sed do eiusmod tempor
      incididunt ut labore et dolore magna aliqua. Ut enim ad
      minim veniam, quis nostrud exercitation ullamco laboris
      nisi ut aliquip ex ea commodo consequat. Duis aute irure
      dolor in reprehenderit in voluptate velit esse cillum
      dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia
      deserunt mollit anim id est laborum. </p>
    <h2>Chapitre 1. HTML</h2>
    <h3>Première introduction</h3>
    <p>Fini !</p>
    <h2>Chapitre 2. CSS</h2>
    <p>En cours...</p>
  </main>  <section class="robots" id="robots1">
    <h1>Nos Robots 1 - flex</h1>
    <p class="voir">voir <code>robots.css ⬎</code></p>
    <div class="flex">
      <div style="background-image: url(src/assets/2017.jpg);">
        <h4>2017</h4>
      </div>
      <div style="background-image: url(src/assets/2018.png);">
        <h4>2018</h4>
      </div>
      <div style="background-image: url(src/assets/2019.png);">
        <h4>2019</h4>
      </div>
      <div style="background-image: url(src/assets/2020.jpg);">
        <h4>2020</h4>
      </div>
      <div style="background-image: url(src/assets/2022.jpg);">
        <h4>2022</h4>
      </div>
      <div style="background-image: url(src/assets/2023.jpg);">
        <h4>2023</h4>
      </div>
    </div>
  </section>
  <section class="layout" id="robots2">
    <h1>Nos Robots 2 - grid</h1>
    <div class="grid">
      <div style="background-image: url(src/assets/2017.jpg);"></div>
      <div class="text">
        <h2>Robot de 2017</h2>
        <p>
          Description. Lorem ipsum dolor sit amet,
          consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <p> Description du robot conclusion. Lorem ipsum dolor sit amet.
        </p>
      </div>
      <div class="subtitle">
        <p>Nous avons fini la compétition classé à la position 10 et nous avons été qualifié pour la suite !      </p>
      </div>
    </div>

    <div class="grid right">
      <div style="background-image: url(src/assets/2022.jpg);"></div>
      <div class="text">
        <h2>Robot de 2022</h2>
        <p>
          Description. Lorem ipsum dolor sit amet,
          consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <p> Description du robot conclusion. Lorem ipsum dolor sit amet.
        </p>
      </div>
      <div class="subtitle">
        <p>Nous avons fini la compétition classé à la position 10 et nous avons été qualifié pour la suite !</p>
      </div>
    </div>

    <div class="grid">
      <div style="background-image: url(src/assets/2023.jpg);"></div>
      <div class="text">
        <h2>Robot de 2023</h2>
        <p>
          Description. Lorem ipsum dolor sit amet,
          consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <p> Description du robot conclusion. Lorem ipsum dolor sit amet.
        </p>
      </div>
      <div class="subtitle">
        <p>Nous avons fini la compétition classé à la position 10 et nous avons été qualifié pour la suite !</p>
      </div>
    </div>
  </section>

	<BaseFooter />

</template>

<style scoped>
p {
  text-align: justify;
}

p.voir {
  text-align: center;
  margin: 0;
}

main {
  padding: 20px;
  width: 600px;
  margin: auto;
}

main img {
  display: block;
  margin: 20px auto;
}

span {
  color: blueviolet;
}

.robots {
  width: 620px;
  margin: auto;
}

@media screen and (max-width: 700px) {
  main {
    width: auto;
  }

  .robots {
    width: auto;
  }
}

.flex {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 4px;
}

/* Pour Nos Robots 1 */

.robots .flex div,
.grid div:first-child {
  width: 200px;
  height: 200px;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  border: 2px solid #ccc;
  border-radius: 10px;
  display: flex;
  align-items: flex-end;
  justify-content: end;
}

.robots .flex div h4 {
  color: white;
  text-align: center;
  margin: 5px;
}

/* Pour Nos Robots 2 */

.robots .flex img {
  border-radius: 10px;
}

.layout {
  width: 620px;
  margin: auto;
}

.grid {
  display: grid;
  border-left: 5px solid #0651b590;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: 200px min-content;
  grid-template-areas:
    "img text"
    "ft ft";
  padding: 5px 15px;
  gap: 10px 0;

  margin: 20px 0;
}

.grid div {
  padding: 0 10px;
}

.grid div:first-child {
  height: 200px;
  grid-area: img;
}

.grid.right {
  grid-template-columns: 3fr 1fr;
  grid-template-areas:
    "text img"
    "ft ft";

  border: 0;
  border-right: 5px solid #d2344290;
}

.grid .text {
  grid-area: text;

  font-size: 0.9rem;
}

.grid .subtitle {
  grid-area: ft;

  font-size: 0.8rem;
  color: #000a;
  background-color: #6d83a150;
  border-radius: 10px;
  padding: 0 10px;
}

@media screen and (max-width: 630px) {
  /* 
  Complète pour que tout le contenu soit lisible. 
   * tu peux modifier la taille de l'image mais ellle doit toujours être bien visible.
   * tu peux enlever les bordures gauches et droite que j'ai mis.
   * tu peux changer complétement le layout actuel, mais je veux 
      * ne perdre aucun contenu
      * qu'il y ait une variation avec les divs ayant la classe .right (même si ça n'a plus rien à voir avec la droite.)
  
  Indice : il va falloir modifier la grille !
  
  */
}
</style>
