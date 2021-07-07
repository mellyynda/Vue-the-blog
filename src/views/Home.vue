<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
import PostList from "../components/PostList.vue";

export default {
  name: "Home",
  components: {
    PostList,
  },
  setup() {
    const posts = ref([
      {
        title: "the last vampire",
        date: "long time ago",
        text: "bla bla vampire bla. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus aliquam molestie nibh sit amet elementum. Nunc magna lorem, eleifend non sem nec, pellentesque feugiat lectus. Mauris felis est, feugiat ac tempus non, scelerisque ut purus. Sed lobortis erat nec felis fringilla, in mollis quam sollicitudin. In quis ullamcorper velit. Nullam tempus euismod massa id scelerisque. Nulla in tempor leo. Duis vel urna sed metus suscipit ultrices vel vel magna. Aenean sodales vehicula eros nec viverra. Cras a tempor libero, nec consequat est. Nam a vulputate dolor. Vivamus sed nisi congue, vulputate sapien eu, consequat nunc. Aliquam in lectus nec diam porta fermentum quis id nisi. Nullam facilisis quis dolor vitae euismod. Praesent interdum porttitor aliquam. Fusce at euismod velit. Cras non hendrerit velit. Fusce nisi elit, varius quis nunc nec, porttitor bibendum nisl. Mauris eu consectetur mi. Nullam congue tortor vitae nisl scelerisque sodales. Phasellus eu molestie risus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque commodo faucibus dapibus. Cras viverra quis augue nec tempor. Nam rutrum volutpat tortor, vitae ornare arcu tristique vitae. Aenean mauris ex, pretium nec metus non, aliquet ultricies nibh. Integer condimentum enim turpis, ac vestibulum dolor mollis at. Curabitur malesuada massa lectus, sed malesuada ante volutpat non.",
        id: 1,
      },
      {
        title: "ultimate shit",
        date: "every couple'a days",
        text: "shitty shit shit shoot. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus aliquam molestie nibh sit amet elementum. Nunc magna lorem, eleifend non sem nec, pellentesque feugiat lectus. Mauris felis est, feugiat ac tempus non, scelerisque ut purus. Sed lobortis erat nec felis fringilla, in mollis quam sollicitudin. In quis ullamcorper velit. Nullam tempus euismod massa id scelerisque. Nulla in tempor leo. Duis vel urna sed metus suscipit ultrices vel vel magna. Aenean sodales vehicula eros nec viverra. Cras a tempor libero, nec consequat est. Nam a vulputate dolor. Vivamus sed nisi congue, vulputate sapien eu, consequat nunc. Aliquam in lectus nec diam porta fermentum quis id nisi. Nullam facilisis quis dolor vitae euismod. Praesent interdum porttitor aliquam. Fusce at euismod velit. Cras non hendrerit velit. Fusce nisi elit, varius quis nunc nec, porttitor bibendum nisl. Mauris eu consectetur mi. Nullam congue tortor vitae nisl scelerisque sodales. Phasellus eu molestie risus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque commodo faucibus dapibus. Cras viverra quis augue nec tempor. Nam rutrum volutpat tortor, vitae ornare arcu tristique vitae. Aenean mauris ex, pretium nec metus non, aliquet ultricies nibh. Integer condimentum enim turpis, ac vestibulum dolor mollis at. Curabitur malesuada massa lectus, sed malesuada ante volutpat non.",
        id: 2,
      },
      {
        title: "rainbows and perfume",
        date: "every day",
        text: "red orange yellow green blue indigo violet and a nice touch of lavander. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus aliquam molestie nibh sit amet elementum. Nunc magna lorem, eleifend non sem nec, pellentesque feugiat lectus. Mauris felis est, feugiat ac tempus non, scelerisque ut purus. Sed lobortis erat nec felis fringilla, in mollis quam sollicitudin. In quis ullamcorper velit. Nullam tempus euismod massa id scelerisque. Nulla in tempor leo. Duis vel urna sed metus suscipit ultrices vel vel magna. Aenean sodales vehicula eros nec viverra. Cras a tempor libero, nec consequat est. Nam a vulputate dolor. Vivamus sed nisi congue, vulputate sapien eu, consequat nunc. Aliquam in lectus nec diam porta fermentum quis id nisi. Nullam facilisis quis dolor vitae euismod. Praesent interdum porttitor aliquam. Fusce at euismod velit. Cras non hendrerit velit. Fusce nisi elit, varius quis nunc nec, porttitor bibendum nisl. Mauris eu consectetur mi. Nullam congue tortor vitae nisl scelerisque sodales. Phasellus eu molestie risus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque commodo faucibus dapibus. Cras viverra quis augue nec tempor. Nam rutrum volutpat tortor, vitae ornare arcu tristique vitae. Aenean mauris ex, pretium nec metus non, aliquet ultricies nibh. Integer condimentum enim turpis, ac vestibulum dolor mollis at. Curabitur malesuada massa lectus, sed malesuada ante volutpat non.",
        id: 3,
      },
    ]);

    return { posts };
  },
};
</script>
