<template>
  <div id="app">
     <div class="main">
        <SiderBar/>
        <div class="right">
          <Header/>
          <StoreCatalog/>
        </div>
     </div>
     <div class="form_detail">
      <Form/>
     </div>
  </div>
</template>

<script>
import SiderBar from '../src/views/SiderBar.vue'
import Header from '../src/views/Header.vue'
import StoreCatalog from '../src/views/StoreCatalog.vue'
import Form from '../src/views/Form.vue'

export default {
  components: {
    SiderBar,
    Header,
    StoreCatalog,
    Form
  }
}
</script>

<style>

/* Reset page */
*{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: Text-Regular;
  font-size: 13px;
}

#app {
  margin: 0px;
  padding: 0px;
  width: 100%;
  height: 100vh;
  display: flex;
}

.main {
  display: flex;
  flex: 1;
  position: relative;
}

.right {
  flex: 1;
}

.form_detail  {
  position: absolute;
  z-index: 1;
  width: 100%;
  height: 100%;
}

</style>
