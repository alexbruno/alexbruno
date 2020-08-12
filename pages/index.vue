<template>
  <div class="flex items-center justify-center h-screen">
    <div class="bg-white rounded-lg shadow-lg p-5 text-center">
      <figure>
        <img
          src="@/assets/img/avatar.jpg"
          class="h-32 w-32 m-auto rounded-full"
          :alt="name"
        />
        <figcaption class="font-bold text-2xl">{{ name }}</figcaption>
      </figure>

      <div class="mt-5 text-gray-700">
        <p>Em construção...</p>
        <p>Under construction...</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    name: 'Alex Bruno Cáceres',
  }),
}
</script>
