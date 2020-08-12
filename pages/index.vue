<template>
  <div class="flex items-center justify-center h-screen">
    <web-card tag="main" class="text-center">
      <web-avatar />

      <div class="my-5 text-gray-600">
        <p>Em construção...</p>
        <p>Under construction...</p>
      </div>

      <web-btn-link to="readme" label="Sobre - About" />
    </web-card>
  </div>
</template>

<script>
export default {
  data: () => ({ name: 'Alex Bruno Cáceres' }),
}
</script>
