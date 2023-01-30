<script setup>
import { ref } from "vue";

const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue",
};

const p = ref(person);

function addToCount() {
  p.value.age = p.value.age + 1;
}

function subtractFromCount() {
  p.value.age = p.value.age - 1;
}
</script>

<template>
  <main>
    <div>
      <h2>Name: {{p.firstName}}</h2>
      <h2>Last: {{p.lastName}}</h2>
      <h1>{{ p.age }}</h1>
      <button @click="subtractFromCount()">-</button>
      <button @click="addToCount()">+</button>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  width: 100vw;
  height: 100vm;
  align-items: center;
  justify-content: center;
}

div {
  margin-top: 10%;
  text-align: center;
}
</style>
