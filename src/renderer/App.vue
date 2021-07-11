<template >
  <div class="app">
    <el-button type="primary">按钮</el-button>
    <navigator />
    <router-view> </router-view>
  </div>
</template>

<script lang=ts>
import { defineComponent } from 'vue'
import Navigator from '/@/components/HomeNavigator.vue'

export default defineComponent({
  components: {
    Navigator
  }
})
</script>

<style>
</style>
