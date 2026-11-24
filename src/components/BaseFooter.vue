<template>
  <footer>
    <p>Contact</p>
    <div class="flex">
      <i class="fa-brands fa-instagram"></i>
      <i class="fa-brands fa-facebook"></i>
      <i class="fa-brands fa-linkedin"></i>
      <i class="fa-brands fa-youtube"></i>
    </div>
    <p>[VOTRE PRÉNOM]</p>

  </footer>
</template>

<style scoped>
footer {
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}

footer p {
  margin: 0 10px;
}

footer .flex {
  display: flex;
  justify-content: space-around;
  max-width: 800px;
  margin: 0 auto;
}

footer .flex i {
  color: white;
  font-size: 1.5rem;
  margin: 0 25px;
  transition: font-size 1s ease;
  min-width: 4rem;
  text-align: center;
  line-height: 3rem;
  cursor: pointer;
}

footer .flex i:hover {
  font-size: 3rem;
}

footer {
  margin-top: 15px;
  background-color: #6d83a1;
  padding: 5px;
}

footer p {
  color: white;
  text-align: right;
}

footer p:first-child {
  text-align: left;
}
</style>
