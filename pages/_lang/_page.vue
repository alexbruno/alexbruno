<template>
  <main class="container m-auto">
    <web-card tag="article" class="my-8">
      <web-avatar />

      <nav class="text-center my-4">
        <nuxt-link to="/" class="text-3xl">🏠</nuxt-link>
      </nav>

      <nuxt-content :document="content" />
    </web-card>
  </main>
</template>

<script>
export default {
  async asyncData({ route, $content }) {
    const { lang, page } = route.params
    const content = await $content(lang, page).fetch()
    const test = await $content('/', { deep: true }).fetch()

    return { content, test }
  },
}
</script>
