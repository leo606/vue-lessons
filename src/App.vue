<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  data() {
    return {
      users: [
        { name: 'user one', age: 12, isActive: false },
        { name: 'user two', age: 20, isActive: true },
        { name: 'user three', age: 23, isActive: true }
      ]
    }
  },
  methods: {

  }
})
</script>

<template>
  <section>
    <li v-for="user in users" :class="{ active: user.isActive }" >
      {{ user.name }}
    </li>
  </section>
</template>

<style scoped>
section {
  padding: 20px;
}

.active {
  background-color: aquamarine;
}
</style>
