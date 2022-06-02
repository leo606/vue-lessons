<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  data() {
    return {
      count: 0
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
<button @click="increment">{{count}}</button>
</template>

<style>
@import './assets/base.css';
</style>
