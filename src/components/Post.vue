<template>
  <h1>{{ title }}</h1>
  <p>{{ content }}</p>
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
