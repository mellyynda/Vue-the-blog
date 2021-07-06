<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search" />
    <p>search term {{ search }}</p>
    <div v-for="name in matchingNames" :key="name">
      <h3>{{ name }}</h3>
    </div>
    <button @click="stopAllWatch">stop watch</button>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
import { computed, watch, watchEffect } from "@vue/runtime-core";

export default {
  name: "Home",
  setup() {
    const search = ref("");
    const names = ref(["Mely", "John", "Tudor", "Darius", "Octavian", "Matei"]);

    const stopWatch = watch(search, () => {
      console.log("watch search ran, search is:", search.value);
    });

    const stopEffect = watchEffect(() => {
      console.log('watch effect ran', search.value);
    });

    const matchingNames = computed(() => {
      return names.value.filter((name) => name.includes(search.value.trim()));
    });

    const stopAllWatch = () => {
      stopWatch();
      stopEffect();
    };

    return { names, search, matchingNames, stopAllWatch };
  },
};
</script>
