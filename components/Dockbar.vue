<script setup lang="ts">

interface dataInterface {}
const data = ref([
  {
   "url": "aa",
   "icon": "aa",
  },
  {
    "url": "aaa",
    "icon": "aa",
  },
  {
    "url": "aaaa",
    "icon": "aa",
  },
  {
    "url": "aaaaa",
    "icon": "aa",
  },
  {
    "url": "aaaaa",
    "icon": "aa",
  },
  {
    "url": "aaaaa",
    "icon": "aa",
  },
  {
    "url": "aaaaa",
    "icon": "aa",
  },
  {
    "url": "aaaaa",
    "icon": "aa",
  },
  {
    "url": "aaaa",
    "icon": "aa",
  }
])
</script>

<template>
  <div class="dockbar">
    <div v-for="(item, index) in data" :key="index" class="item"> {{data.url}}</div>
  </div>
</template>

<style scoped>
.dockbar {
  width: 5vw;

  & .item {
    width: 5vw;
  }


}
</style>