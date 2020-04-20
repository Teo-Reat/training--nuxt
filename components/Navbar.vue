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
      <li class="mr-6">
        <nuxt-link class="text-blue-500 hover:text-blue-800" to="/users" active-class="font-bold">
          Users
        </nuxt-link>
      </li>
      <li v-if="!hasToken" class="mr-6">
        <nuxt-link class="text-blue-500 hover:text-blue-800" to="/login">
          Login
        </nuxt-link>
      </li>
      <li v-else class="mr-6">
        <a class="text-blue-500 hover:text-blue-800" href="#" @click="logout">
          Logout
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  computed: {
    hasToken () {
      return this.$store.getters.hasToken
    }
  },
  methods: {
    logout () {
      this.$store.dispatch('logout')
      this.$router.push('/login')
    }
  }
}
</script>

<style scoped>

</style>
