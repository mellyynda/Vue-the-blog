<template>
  <div class="home">
    <p ref="p" @click="logRef">
      My name is {{ name }} and I am {{ age }} years old.
    </p>
    <button @click="handleClick">click me</button>
    <input type="text" v-model="name">
    <button @click="age++">+</button>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";

export default {
  name: "Home",
  setup() {
    const p = ref(null);

    const name = ref("mario");
    const age = ref(30);

    const handleClick = () => {
      name.value = "louigi";
      age.value = 45;
    };

    return { name, age, handleClick, p };
  },
};
</script>
