<script setup>
import LoginPage from "./LoginPage.vue";
</script>
<template>
  <LoginPage />
</template>

<style>
html,
body,
/* app 容器占据全部空间，无内外边距*/
#app {
  height: 100%;
  margin: 0;
  padding: 0;
}
/* 宽高以 border 为准*/
* {
  box-sizing: border-box;
}
</style>
