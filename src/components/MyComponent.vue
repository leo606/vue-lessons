<template>
  <h2> {{text}} </h2>
</template>

<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  props: {
    text: {
      type: String,
      default: 'default text'
    }
  }
})
</script>