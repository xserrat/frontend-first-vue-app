<template>
  <div>
    <h1>Last posts:</h1>
    <PostsList />
  </div>
</template>

<script lang="ts">
import PostsList from "@/components/PostsList.vue";
import { defineComponent } from "vue";
export default defineComponent({
  name: "Home",
  components: {
    PostsList,
  },
});
</script>
