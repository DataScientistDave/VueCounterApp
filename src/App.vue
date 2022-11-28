<script setup>
import { ref } from "vue";

const count = ref(0);
const addFunc = () => {
  console.log(count);
  count.value++;
};
</script>



<template>
  <div class="container">
    <h4>The current count is ...</h4>
    <h1>{{ count }}</h1>
    <div class="buttons-div">
      <button v-on:click="count--">-</button>
      <button @click="addFunc()">+</button>
    </div>
  </div>
</template>

<!-- <script>
export default {
  name: "App",
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    addFunc() {
      this.count++;
    },
  },
};
</script> -->

<style scoped>
.container {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: aliceblue;
}

.buttons-div {
  display: flex;
}
</style>