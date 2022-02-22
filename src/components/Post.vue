<template>
  <article>
    <h2>{{ title }}</h2>
    <p>{{ content }}</p>
  </article>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "Post",
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      title: "",
      content: "",
    };
  },
  created() {
    this.title = this.post.title;
    this.content = this.post.content;
  },
});
</script>
