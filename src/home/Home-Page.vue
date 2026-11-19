<script setup>
import BaseHeader from '../components/BaseHeader.vue'
import Welcome from '../components/Welcome.vue'
import BaseFooter from '../components/BaseFooter.vue'
</script>

<template>
  <header>
		<BaseHeader />
  </header>
  <main>
		<h1>Ceci est la page principale de mon site web</h1>
    <Welcome msg="Bravo! Tu as créé une page"/>
  </main>
	<footer>
		<BaseFooter />
	</footer>
</template>

<style scoped>
/* Inclure ici le css spécifique à cette page
Du scss (css mais un peu plus pratique) peut être utilisé en instalant un
package en plus et en ajoutant `lang="scss"` dans la balise style */
</style>
