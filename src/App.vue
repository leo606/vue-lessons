<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  data() {
    return {
      count: 0,
      name: 'Counter'
    }
  },
  methods: {
    increment() {
      this.count += 1
    }
  }
})
</script>

<template>
  <section>
    <h1>{{ name }}</h1>
    <button @click="increment">{{ count }}</button>
  </section>
</template>

<style scoped>
  section {
    padding: 20px;
  }

  button {
    padding: 1em;
    min-width: 6em;
    font-size: 2em;
    font-weight: 900;
  }
</style>
