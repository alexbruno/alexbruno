<template>
  <main class="container m-auto">
    <web-card tag="article" class="my-8">
      <web-avatar />

      <div class="text-center my-4">
        <web-btn-link to="/" label="Início - Home" />
      </div>

      <p class="py-1 mb-4 border-b">
        <span>Github:</span>
        <strong>alexbruno</strong>
      </p>

      <nuxt-content class="content" :document="readme" />
    </web-card>
  </main>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const readme = await $content('readme').fetch()
    return { readme }
  },
}
</script>
