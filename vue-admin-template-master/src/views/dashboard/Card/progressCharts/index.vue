<template>
    <div class="charts" ref="charts"></div>
  </template>
  
  <script>
  import*  as echarts  from "echarts";
  
  export default {
     name:'barCharts',
     mounted() {
      
      //初始化echarts实例
      let barCharts=echarts.init(this.$refs.charts);
  
      barCharts.setOption({
          xAxis:{ show:false,
            min:0,
            max:100,
         },
          yAxis:{
              show:false,
              type:'category',

          },
          series:[
              {
                  type:'bar',
                  data:[70],
                  //拐点样式
                  color:"pink",
                  barWidth:10,
                  showBackground:true,
                  backgroundStyle:{
                    color:'#eee'
                  },
                  label:{
                    show:true,
                    formatter:'|',
                    position:'right'

                  }
               
             
              }
          ],
          grid:{
              left:0,
              top:0,
              right:0,
              bottom:0,
          }
      })
     },
  }
  </script>
  
  <style scoped>
  .charts{width: 100%; height: 100%;}
  
  
  </style>