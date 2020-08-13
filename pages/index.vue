<template>
  <div class="flex items-center justify-center h-screen">
    <web-card tag="main" class="text-center">
      <web-avatar class="mb-5" />

      <nav class="flex justify-around">
        <web-btn-link
          v-for="lang in langs"
          :key="lang"
          :to="lang"
          :label="lang"
        />
      </nav>
    </web-card>
  </div>
</template>

<script>
export default {
  data: () => ({ name: 'Alex Bruno Cáceres' }),

  async asyncData({ $content }) {
    const content = await $content('/', { deep: true }).fetch()
    const dir = content.filter((i) => i.dir !== '/').map((i) => i.dir)
    const langs = [...new Set(dir)]

    return { langs }
  },
}
</script>
