<script setup lang="ts">
import FlipList from "./components/FlipList.vue";
import Tabs from "./components/Tabs.vue";
</script>

<template>
  <div>
    <FlipList />
    <div class="py-4 bg-beige-base">
      <Tabs />
    </div>
  </div>
</template>

<style scoped>
.bg-beige-base {
  --tw-bg-opacity: 0.7;
  background-color: rgb(237 220 203 / var(--tw-bg-opacity));
}
</style>
