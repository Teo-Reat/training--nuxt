<template>
  <section>
    <h1>User {{ user.data.name }}</h1>
    <h2>{{ user.data.email }}</h2>
  </section>
</template>

<script>
export default {
  validate ({ params }) {
    return /^\d+$/.test(params.id)
  },
  async asyncData ({ $axios, params }) {
    const user = await $axios.get('https://jsonplaceholder.typicode.com/users/' + params.id)
    return { user }
  }
}
</script>

<style scoped>

</style>
