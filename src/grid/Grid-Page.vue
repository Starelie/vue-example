<script setup>
import BaseHeader from '../components/BaseHeader.vue'
import BaseFooter from '../components/BaseFooter.vue'
</script>

<template>

	<BaseHeader />

  <div class="grid-container">
    <div class="days">
      <div class="day-label">Lundi</div>
      <div class="day-label">Mardi</div>
      <div class="day-label">Mercredi</div>
      <div class="day-label">Jeudi</div>
      <div class="day-label">Vendredi</div>
    </div>
    <div class="hours">
      <div class="hour-label">08:30</div>
      <div class="hour-label">09:30</div>
      <div class="hour-label">10:30</div>
      <div class="hour-label">11:30</div>
      <div class="hour-label">12:30</div>
      <div class="hour-label">13:30</div>
      <div class="hour-label">14:30</div>
      <div class="hour-label">15:30</div>
      <div class="hour-label">16:30</div>
      <div class="hour-label">17:30</div>
      <div class="hour-label">18:30</div>
      <div class="hour-label">19:30</div>
      <div class="hour-label">20:30</div>
      <div class="hour-label">21:30</div>
    </div>
    <div class="slots">
      <div class="lundi debut13h fin16h"></div>
      <div class="vendredi debut8h fin12h"></div>
      <div class="vendredi debut13h fin16h"></div>
    </div>
  </div>

	<BaseFooter />

</template>

<style scoped>
body {
  background-color: ghostwhite;
  text-align: center;
}


.grid-container {
  display: grid;
  grid-template-columns: auto repeat(5, 1fr);
  /* Une colonne pour les heures, puis une colonne pour chaque jour */
  grid-template-rows: auto;
  /* Une ligne pour les jours, une ligne pour les heures */
}

.days {
  grid-row: 1;
  /* La première rangée */
  grid-column: 2 / -1;
  /* Deuxième colonne jusqu'à la dernière */
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  /* Une colonne pour chaque jour */
}

.hours {
  grid-column: 1;
  /* La première colonne */
  grid-row: 2 / -1;
  /* Deuxième ligne jusqu'à la dernière */
  display: grid;
  grid-template-rows: repeat(14, 6vh);
  /* Une ligne pour chaque heure */
}

.hours>div {
  width: min-content;
}

.slots {
  grid-column: 2 / -1;
  grid-row: 2 / -1;
  display: grid;
  grid-template-rows: repeat(14, 6vh);
  /* Une ligne pour chaque heure */
  grid-template-columns: repeat(5, 1fr);
  /* Une colonne pour chaque jour */
}

.slots>div {
  background-color: cornflowerblue;
  border-radius: 5px;
  margin: 0 5px;
}

/* À COMPLÉTER */
.lundi {
  grid-column: 1;
}

.vendredi {
  grid-column: 5;
}

.debut13h {
  grid-row-start: 6;
}

.fin16h {
  grid-row-end: 9;
}

.debut8h {
  grid-row-start: 1;
}

.fin12h {
  grid-row-end: 5;
}
</style>
