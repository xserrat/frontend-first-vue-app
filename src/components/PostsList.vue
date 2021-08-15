<template>
  <div :key="post.id" v-for="post in posts">
    <Post :post="post" />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import Post from "@/components/Post.vue";

export default defineComponent({
  name: "PostsList",
  components: {
    Post,
  },
  data() {
    return {
      posts: [],
    };
  },
  async created() {
    const result = await fetch("http://localhost:5000/posts");

    this.posts = await result.json();
  },
});
</script>
