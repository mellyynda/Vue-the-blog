<template>
  <div class="home">
    <h1>Home</h1>
    <div v-if="error">{{ error }}</div>
    <div v-if="posts.length">
      <PostList :posts="posts" />
    </div>
    <div v-if="!posts.length && !error">
      <h4>content loading, please wait...</h4>
    </div>
  </div>
</template>

<script>
import getPosts from "../composables/getPosts";
import PostList from "../components/PostList.vue";

export default {
  name: "Home",
  components: {
    PostList,
  },
  setup() {
    const { posts, error, load } = getPosts();

    load();

    return { posts, error };
  },
};
</script>
