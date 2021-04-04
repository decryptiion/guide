<template>
  <div id="app">
    <Tabs></Tabs>
  </div>
</template>

<script>
  import Tabs from '@/components/Tabs'

  export default {
    name: 'App',
    components: {
      Tabs
    }
  }
</script>

<style scoped>
  body {
    background-image: url('assets/bg.png');
    font-family: 'Roboto', sans-serif;
  }
  #app {
    background: rgba(0, 0, 0, 0.25);
    width: 60vw;
    height: 70vh;
    margin-top: 15vh;
    margin-left: 20vw;
    border-radius: 5px;
  }
</style>