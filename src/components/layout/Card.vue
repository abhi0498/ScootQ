<template>
    <mdb-card class="card-body" style="width: 22rem; margin-top: 1rem;">
        <div class='row'>
            <div class='col'>
    <mdb-card-title>{{title}}</mdb-card-title>
    <mdb-card-text><strong>{{text}}</strong></mdb-card-text>
            </div>
            <div class='col'>
               <mdb-icon size='4x'  :icon=icon />
            </div>

        </div>

  </mdb-card>
</template>

<script>
  import { mdbCard,mdbIcon ,mdbCardTitle, mdbCardText } from 'mdbvue';
  export default {
    name: 'Card',
    components: {
      mdbCard,
      mdbCardTitle,
      mdbCardText,mdbIcon
    },
    props:['title','text','icon']
  }
</script>

<style>

</style>