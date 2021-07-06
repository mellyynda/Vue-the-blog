<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ person.name }} ◈ {{ person.age }}</p>
    <button @click="updatePerson">Be younger</button>
    <h2>Reactive</h2>
    <p>{{ personTwo.name }} ◈ {{ personTwo.age }} ◈ {{ nameTwo }}</p>
    <button @click="updatePersonTwo">Make younger</button>
  </div>
</template>

<script>
import { reactive, ref } from "@vue/reactivity";

export default {
  name: "Home",
  setup() {
    const person = ref({ name: "Mely", age: 32 });
    const personTwo = reactive({ name: "John", age: 37 });
    let nameTwo = reactive("Juxiela");

    const updatePerson = () => {
      person.value.age = 28;
    };

    const updatePersonTwo = () => {
      personTwo.age = 30;
    }

    return { person, updatePerson, personTwo, updatePersonTwo, nameTwo };
  },
};
</script>
