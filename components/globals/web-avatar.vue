<template>
  <figure class="flex flex-col items-center justify-center">
    <img
      src="@/assets/img/avatar.jpg"
      class="h-32 w-32 rounded-full"
      :alt="name"
    />
    <figcaption class="text-2xl">{{ name }}</figcaption>
  </figure>
</template>

<script>
export default {
  name: 'web-avatar',

  data: () => ({ name: 'Alex Bruno Cáceres' }),
}
</script>
