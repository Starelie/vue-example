<script setup>
import BaseHeader from '../components/BaseHeader.vue'
import Welcome from '../components/Welcome.vue'
import BaseFooter from '../components/BaseFooter.vue'
</script>

<template>
  <BaseHeader />
  <main>
    <h1>Ceci est la page principale de mon site web</h1>
    <Welcome v-bind:color="green">
      <template v-slot:text>
        Bravo! Tu as créé une page!
      </template>
    </Welcome>
  </main>
  <BaseFooter />
</template>

<style scoped lang="scss">
/* Inclure ici le css spécifique à cette page */
</style>
