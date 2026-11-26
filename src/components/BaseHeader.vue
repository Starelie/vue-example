<template>
  <header>
    <nav role="navigation" class="horinav">
      <p class="voir">voir <code>menuCorrection.css ⬎</code></p>
      <ul>
        <li><a href="/index.html"> Accueil <i class="fa-solid fa-house"></i></a>
          <ul>
            <a href="#robots1">
              <li>Nos Robots 1</li>
            </a>
            <a href="#robots2">
              <li>Nos Robots 2</li>
            </a>
            <a href="/grid.html">
              <li>Grid</li>
            </a>
          </ul>
        </li>
        <li><a href="#">Compétitions</a>
          <ul>
            <a href="#">
              <li>2016</li>
            </a>
            <a href="#">
              <li>2017</li>
            </a>
            <a href="#">
              <li>2018</li>
            </a>
            <a href="#">
              <li>2019</li>
            </a>
            <a href="#">
              <li>2020-2021</li>
            </a>
            <a href="#">
              <li>2022</li>
            </a>
          </ul>
        </li>
        <li><a href="#">Notre Équipe</a>
          <ul>
            <a href="#">
              <li>Rejoindre</li>
            </a>
            <a href="#">
              <li>Organisation</li>
            </a>
          </ul>
        </li>
      </ul>
    </nav>
    <h2>Cours 5</h2>
  </header>
</template>

<style scoped lang="scss">
/* MENU */

nav a {
  text-decoration: none;
}

nav ul {
  background: transparent;
  list-style: none;
  margin: 0;
  padding-left: 0;
  font-size: 120%;
}

nav {
  float: right;
  display: block;
  margin-top: 7px;
}

a {
  color: inherit;
}

nav li {
  color: inherit;
  background: transparent;
  display: block;
  float: left;
  font-size: 90%;
  padding: 0.7rem;
  margin: 0.1rem;
  position: relative;
  text-decoration: none;
  transition-duration: 0.5s;
  border-radius: 15px;

}

.horinav li ul li:hover {
  background-color: transparent;
  color: #c33;
  font-weight: 700;
}

.horinav li:hover {
  background-color: #c33;
  color: white;
  border-radius: 25px 25px 0px 0px;
  transition: all 0.5s ease;
}

/* ul li ul li:hover {
  background: #000;
  color: white;
  cursor: pointer;
} */

/*#DB2B39*/

nav ul li ul {
  color: #212b43;
  background: white;
  border-radius: 0 0px 15px 15px;
  width: 100%;
  position: absolute;
  transition: all 0.5s ease;
  margin-top: 0.6rem;
  left: 0;
  display: none;
  font-size: 80%
}

ul li:hover>ul,
ul li:focus-within>ul,
ul li ul:hover,
ul li ul:focus {
  visibility: visible;
  opacity: 1;
  display: block;
  transition: all 1s ease;
}

ul li ul li {
  margin-left: 0px;
  clear: both;
  width: 90%;
  padding: 0.5em;
}

@media screen and (max-width: 500px) {
  .horinav {
    margin: auto;
    clear: both;
  }

  header h2 {
    text-align: center;
    height: min-content;
    margin-left: auto;
  }
}

header p.voir {
  margin: 0;
  position: absolute;
  top: 0;
  right: 5px;
}

header {
  margin: 0;
  background-color: #6d83a1;
  padding: 5px;
  color: white;
}

header h2 {
  text-align: left;
  margin-left: 20px;
}

header h3 {
  display: inline;
}
</style>
