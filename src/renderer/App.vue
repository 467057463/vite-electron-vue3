<template lang="pug">
.app
  router-link(to="/") 首页
  router-link(to="/about") about
  router-link(to="/view") webview
  router-view
</template>

<script setup lang="ts">
import { ref } from 'vue'
const test1 = 'test'
const test = ref(0)
</script>

<style>
</style>
