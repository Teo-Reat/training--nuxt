<template>
  <div>
    <ul class="flex">
      <li class="mr-6">
        <nuxt-link class="text-blue-500 hover:text-blue-800" to="/" exact active-class="font-bold" no-prefetch>
          Home
        </nuxt-link>
      </li>
      <li class="mr-6">
        <nuxt-link class="text-blue-500 hover:text-blue-800" to="/about" active-class="font-bold">
          About
        </nuxt-link>
      </li>
      <li>
        <nuxt-link class="text-blue-500 hover:text-blue-800" to="/users" active-class="font-bold">
          Users
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
</script>

<style scoped>

</style>
