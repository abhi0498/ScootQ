<template>
    <div class="d-inline">
      <mdb-input type="text" placeholder="Search" aria-label="Search"/>
      
    </div>
</template>

<script>
  import {   mdbInput } from 'mdbvue';
  export default {
      name:'Searchbar',
    components: {
   
      
      mdbInput
    }
  }
</script>

<style scoped>
input{
    width:900px;
}
</style>