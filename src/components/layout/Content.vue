<template>
<div class='content'>

    <Searchbar />

    <h2>Dashboard</h2>
    <div class="cards"> 
    <Card title="Active Users" text='512'  icon="users" />
    <Card title="Total Sales" text='$75000 ' icon='dollar-sign'/>
    <Card title="Changes"  text='25%' icon='chart-line'/>
    </div>

<Chart />
</div>
  
</template>

<script>
import Chart from './Chart'
import Card from './Card'
import Searchbar from './Searchbar'
export default {
    name:'Content',
components:{
    Chart,
    Card,
    Searchbar
}
}
</script>

<style scoped>
.content{
    position: absolute;
    left:20%;
}
.cards{
    display: flex;
    justify-content: space-around;
}
</style>