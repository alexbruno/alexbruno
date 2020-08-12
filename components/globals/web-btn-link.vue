<template>
  <nuxt-link
    :to="to"
    class="text-lg text-teal-500 border border-teal-500 rounded px-3 py-2 hover:bg-teal-500 hover:text-white transition-all duration-500 ease-in-out"
  >
    {{ label }}
  </nuxt-link>
</template>

<script>
export default {
  name: 'web-btn-link',

  props: {
    to: {
      type: String,
      default: null,
    },
    label: {
      type: String,
      default: null,
    },
  },
}
</script>
