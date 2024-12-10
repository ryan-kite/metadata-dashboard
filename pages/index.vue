<script setup lang="ts">
const description = ref('The main landing page.')

// composables with state
const locales = useLocales()
const locale = useLocale()
const date = useLocaleDate(new Date('2016-10-26'))

useHead({
  meta: [
    { name: 'description', content: description }
  ],
})
</script>
<template>
  <section>
    <h1>Home</h1>
    <AppAlert>
      This is an auto-imported component
    </AppAlert>

    <div>
      <h2>Nuxt birthday</h2>
      <p>{{ date }}</p>
      <p>the locale of the doc is: {{ locale }}</p>
      <label for="locale-chooser">Preview a different locale</label>
      <select id="locale-chooser" v-model="locale">
        <option v-for="l of locales" :key="locale" :value="locale">
          {{ l }}
        </option>
      </select>
    </div>
  </section>
</template>
