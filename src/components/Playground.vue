<template>
    <div>
        <h1 v-if="show">
            Playground
        </h1>
        <p>
            {{ message }}
        </p>
        <input v-model="message">
        <button v-on:click="capitalize">
            capitalize
        </button>
    </div>
</template>

<script>
export default {
  name: 'Playground',
  data: () => ({
      show: true,
      message: 'Description'
  }),
  methods: {
      capitalize: function() {
          this.message = this.message.toUpperCase();
      }
  }
}
</script>

<style scoped>

</style>
