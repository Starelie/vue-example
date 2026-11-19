<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="greetings">
    <h1 class="green">Bienvenue</h1>
    <h3>
      {{ msg }}
    </h3>
  </div>
</template>

<style scoped>
/* Inclure ici le css spécifique à cette page */
</style>
