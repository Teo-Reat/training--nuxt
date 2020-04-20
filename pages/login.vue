<template>
  <div>
    <div v-if="$route.query.message" class="bg-red-200">
      Need login first!
    </div>
    <h2 class="text-4xl">
      Login page
    </h2>
    <form @submit.prevent="onSubmit">
      <label>
        <input type="text" class="bg-blue-200 my-4">
      </label>
      <p>
        <nuxt-link to="/">
          To Home Page
        </nuxt-link>
      </p>
      <button type="submit">
        Submit
      </button>
    </form>
  </div>
</template>

<script>
export default {
  layout: 'empty',
  methods: {
    onSubmit () {
      this.$store.dispatch('login')
      this.$router.push('/')
    }
  }
}
</script>

<style scoped>

</style>
