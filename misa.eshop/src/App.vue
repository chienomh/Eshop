<template>
  <div id="app">
    <SiderBar/>
    <Header/>
  </div>
</template>

<script>
import SiderBar from '../src/views/SiderBar.vue'
import Header from '../src/views/Header.vue'


export default {
  components: {
    SiderBar,
    Header
  }
}
</script>

<style>

/* Reset page */
*{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}

#app {
  margin: 0px;
  padding: 0px;
  width: 100%;
  height: 100vh;
  display: flex;
}
</style>
