<script setup lang="ts">

</script>

<template>
  <div class="settings-bar">
    <div class="themes" @click.prevent=" console.log('Test')">
      redacted
    </div>
  </div>

</template>

<style scoped>
.settings-bar {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  height: 100%;
  width: 100%;
  z-index: -1;

  & .themes {
    position: absolute;
    top: 4vw;

    height: 5vw;
    width: 5vw;
    background-color: darkolivegreen;

    transition: all 0.5s ease-in-out;
    transform: translateX(3vw);
    border-radius: 8px;

    background-image: url("../assets/settings-pic.jpg");
    background-size: cover;
  }

  & .themes:hover {
    transform: translateX(0.1vw);
    cursor: pointer;

  }
}

</style>