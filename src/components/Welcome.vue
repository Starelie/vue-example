<script setup>
defineProps({
  color: {
    type: String,
    required: false,
    default: "green",
  },
})
</script>

<template>
  <div class="greetings">
    <h1 :class="color">Bienvenue</h1>
    <h3><slot name="text"></slot></h3>
  </div>
</template>

<style scoped lang="scss">
.green {
  color: green;
}

.blue {
  color: blue;
}

.red {
  color: red;
}

.white {
  color: white;
}

.black {
  color: black;
}
</style>
