<template>
  <div id="app">
    <Sidebar />
   <Content />
  </div>
</template>

<script>

import Sidebar from './components/layout/Sidebar'
import Content from "./components/layout/Content";
export default {
  name: 'App',
  components:{
   Content,
    Sidebar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap');


</style>
