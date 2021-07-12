<template lang="pug">
webview#test(
  src="https://www.baidu.com/"
  style="width:640px; height:480px"
  @did-start-loading="loadstart"
  @did-stop-loading="loadend"
  :preload="pathToInjectScript"
)
</template>

<script lang="ts">
import { useIpc } from '../composables'

// import path from 'path'
// const pathToInjectScript = `file://${path.join(__static, '/inject.js')}`

export default {
  data() {
    return {
      pathToInjectScript: 'ssss'
    }
  },

  mounted() {
    useIpc().send('TEST', 'sfdsaf')
  },

  methods: {
    loadstart() {
      console.log('test')
    },

    loadend() {
      console.log('load end')
    }
  }
}
</script>
