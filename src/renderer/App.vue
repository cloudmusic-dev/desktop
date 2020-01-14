<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
  import { Titlebar, Color } from 'custom-electron-titlebar'

  // eslint-disable-next-line no-new
  new Titlebar({
    backgroundColor: Color.fromHex('#800')
  })

  export default {
    name: 'cloudmusic'
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  body {
    font-family: 'Source Sans Pro', sans-serif;
  }
</style>
