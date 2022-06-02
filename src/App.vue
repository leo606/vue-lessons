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
  <h1>{{ name }}</h1>
  <button @click="increment">{{ count }}</button>
</template>

<style>
  button {
    background-color: blue;
  }
</style>
