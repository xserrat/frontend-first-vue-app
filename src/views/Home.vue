<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
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
