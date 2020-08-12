<template>
  <article>
    <nuxt-content :document="readme" />
  </article>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const readme = await $content('readme').fetch()

    return { readme }
  },
}
</script>
