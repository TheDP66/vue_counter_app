<script setup lang="ts">
import { ref } from "vue";

const count = ref(0);

const addToCount = () => {
  count.value++;
};

const subtractFromCount = () => {
  console.log("count", count);
  count.value--;
};
</script>

<template>
  <main>
    <div>
      <h4>The curernt count is...</h4>
      <h1>{{ count }}</h1>
      <button @click="subtractFromCount">-</button>
      <button @click="addToCount">+</button>
    </div>
  </main>
</template>

<!-- ? scoped:  -->
<style scoped>
main {
  background-color: aliceblue;
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
}

div {
  text-align: center;
}
</style>
