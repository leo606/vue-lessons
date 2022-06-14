<template>
  <MyComponent text="text by prop" />
  <section>
    <li v-for="user in users" :class="{ active: user.isActive }">
      {{ user.name }}
    </li>
    <div ref="randomDiv"></div>
    <button @click="getRandomNumber">Get a random number</button>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue"
import MyComponent from "./components/MyComponent.vue"

export default defineComponent({
  data() {
    return {
      users: [
        { name: "user one", age: 12, isActive: false },
        { name: "user two", age: 20, isActive: true },
        { name: "user three", age: 23, isActive: true },
      ],
    };
  },
  methods: {
    getRandomNumber() {
      const randomNum = Math.ceil(Math.random() * 100);
      const randomDiv = this.$refs.randomDiv as HTMLDivElement;
      randomDiv.innerHTML = randomNum.toString();
    }
  },
  components: { MyComponent }
})
</script>

<style scoped>
section {
  padding: 20px;
}

.active {
  background-color: aquamarine;
}
</style>
