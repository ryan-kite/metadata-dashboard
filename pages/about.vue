<script setup lang="ts">
const description = ref('The about page.')

useHead({
  meta: [
    { name: 'description', content: description }
  ],
})
</script>

<template>
  <section>
    <h1>About</h1>
    <p>This page will be displayed at the /about route.</p>
    <img src="/img/db.png" alt="Discover Nuxt 3" />

  </section>
</template>
