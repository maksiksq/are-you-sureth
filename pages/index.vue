<script setup lang="ts">
const welcome = ref<string>("i wish i knew a person existing near who i'd find enjoyable")
const time = ref<Date>(new Date())

const isLightbox = ref<boolean>(false);

</script>

<template>
  <Lightbox :is-lightbox=isLightbox />
  <Settings/>
  <main class="main-wrapper">
    <div>
      <div class="h-text">
        <h1>{{ welcome }}</h1>
      </div>
      <div class="pic-cover"/>
      <Dockbar/>
      <img src="@/assets/pic.png" alt="beans"/>
      <div class="time">
        <h2>{{ time.toLocaleTimeString("de-De").slice(0, 5) }}</h2>
      </div>
    </div>
    <!--    <Searchbar/>-->
  </main>

</template>
<style>
* {
  font-family: Comfortaa, sans-serif;
  color: #fff;

  margin: 0;
  padding: 0;
}

body, html {
  overflow: hidden;
  background-color: #2e2e2e;

  height: 100%;
  width: 100%;
}

::selection {
  background: #2e2e2e;
}

</style>
<style scoped>
.main-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  z-index: -1;
}

.main-wrapper > div > img {
  position: relative;
  height: 550px;
  width: 550px;
  z-index: 100;

  border: 1px solid #ffffff;
}

.h-text {
  display: flex;
  flex-direction: row;
  justify-content: center;

  & h1 {
    padding: 6px 4px 6px 4px;
    border: aqua solid 1px;
    border-radius: 5px;
    margin-bottom: 3vw;
    margin-top: 4vw;
  }

}

.time {
  display: flex;
  flex-direction: row;
  justify-content: center;
  font-size: 40px;
  letter-spacing: 15px;

  & h2 {
    padding: 3px 2px 3px 2px;
    border: aqua solid 1px;
    border-radius: 5px;
    margin-top: 3vw;

  }
}

</style>