<template>
  <mdb-container>
    <mdb-line-chart :data="lineChartData" :options="lineChartOptions" :width="600" :height="300"></mdb-line-chart>

  </mdb-container>
  
</template>

<script>
import axios from 'axios'



  import { mdbLineChart, mdbContainer } from 'mdbvue';
  export default {
    name: 'Chart',
    components: {
      mdbLineChart,
      mdbContainer
    },
    created(){
      axios.get('https://cors-anywhere.herokuapp.com/canvasjs.com/services/data/datapoints.php?xstart=1&ystart=20&length=40&type=json')
    .then((res)=>{
        this.d='hello'
        let labels=[]
        let data=[]
        let data1=[]
        let i=0;
       for (const d of res.data) {
         labels.push(String(d[0]))

         if(i<=20)
         data.push(d[1])
         else
         data1.push(d[1])
         i+=1
       }


      this.lineChartData=  {          
          labels: labels.slice(0,20),
          datasets: [
            {
              label: "My First dataset",
              backgroundColor: "rgba(255, 99, 132, 0.1)",
              borderColor: "rgba(255, 99, 132, 1)",
              borderWidth: 0.7,
              data: data
            },
            {
              label: "My Second dataset",
              backgroundColor: "rgba(151,187,205,0.2)",
              borderColor: "rgba(151,187,205,1)",
              borderWidth: 0.8,
              data: data1
            }
          ]
      }

    })
    .catch((err)=>{
      this.err=err
    })
    },
    data() {
      return {
          err:'',
          d:'',
        lineChartData: {

        },
        lineChartOptions: {
          responsive: true,
          maintainAspectRatio: false,
          scales: {
            xAxes: [{
              gridLines: {
                display: true,
                color: "rgba(0, 0, 0, 0.1)"
              }
            }],
            yAxes: [{
              gridLines: {
                display: true,
                color: "rgba(0, 0, 0, 0.1)"
              }
            }]
          }
        }
      };
    }
  }
</script>

<style>

</style>