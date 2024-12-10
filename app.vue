<script setup lang="ts">
useHead({
  title: 'My App',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  bodyAttrs: {
    class: 'test'
  },
  script: [{ innerHTML: 'console.log(\'Hello world\')' }]
})

const title = ref('Metadata Dashboard')

const color = useColor()

</script>

<template>
  <div>

    <Head>
      <Title>{{ title }}</Title>
      <Meta name="description" :content="title" />
      <Style type="text/css" children="body { background-color: #D3D3D3; }"></Style>
    </Head>

    <NuxtLayout>
      <p>Current color: {{ color }}</p>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<style>

  .page-enter-active,
  .page-leave-active {
    transition: all 0.4s;
  }

  .page-enter-from,
  .page-leave-to {
    opacity: 0;
    filter: blur(1rem);
  }
</style>
