<template>
  <div class="flex items-center justify-center h-screen">
    <web-card tag="main" class="text-center">
      <web-avatar />

      <nuxt-content class="my-5" :document="content" />

      <nav class="flex justify-around">
        <web-btn-link
          v-for="page in menu"
          :key="page.path"
          :to="page.path"
          :label="page.title"
        />
      </nav>

      <nav class="text-center mt-5">
        <nuxt-link to="/" class="text-3xl">🏠</nuxt-link>
      </nav>
    </web-card>
  </div>
</template>

<script>
export default {
  async asyncData({ route, $content }) {
    const { lang } = route.params
    const index = `/${lang}/index`
    const pages = await $content(lang).fetch()
    const content = pages.find(({ path }) => path === index)
    const menu = pages
      .filter(({ path }) => path !== index)
      .map(({ path, title }) => ({ path, title }))

    return { content, menu }
  },
}
</script>
