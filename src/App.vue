<script setup lang="ts">
import MainView from "./views/MainView.vue";
import { onBeforeMount } from "vue";
import { invoke } from "@tauri-apps/api";

 onBeforeMount(() => {
     invoke("init").then(() => {});
     // document.addEventListener("contextmenu", (event) => event.preventDefault());
 });
</script>

<template>
  <div>
    <div id="main">
      <main-view />
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.el-input__inner {
  line-height: 0px !important;
}

.el-tabs__item {
  font-size: 1.1rem;
  line-height: 30px;
}
</style>
