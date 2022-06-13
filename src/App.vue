<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  data() {
    return {
      users: [
        { name: 'user one', age: 12, isActive: false },
        { name: 'user two', age: 20, isActive: true },
        { name: 'user three', age: 23, isActive: true },
      ],
      randomNumber: 0
    }
  },
  methods: {
    getRandomNumber() {
      this.randomNumber = Math.ceil(Math.random() * 100)
    }
  }
})
</script>

<template>
  <section>
    <li v-for="user in users" :class="{ active: user.isActive }">
      {{ user.name }}
    </li>
    <div> {{ randomNumber }} </div>
    <button @click="getRandomNumber">Get a random number</button>
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
