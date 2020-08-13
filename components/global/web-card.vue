<template>
  <component :is="tag" class="web-card bg-white rounded-lg shadow-lg p-8">
    <slot />
  </component>
</template>

<script>
export default {
  name: 'web-card',

  props: {
    tag: {
      type: String,
      default: 'div',
    },
  },
}
</script>
