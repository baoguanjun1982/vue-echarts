<template>
    <div class="Mmain">
        <h3>
            臭氧用量分布
        </h3>
         <img src="../assets/img/hor-box-border.png">
        <div id="lineChart" class="mycharts" >
        </div>
       
    </div>
   
</template>
<script>
import Echarts from 'echarts'
export default {
    data(){
        return{}
    },
    mounted(){
        this.getmyechars()
    },
    methods:{
        getmyechars(){
         
    //平均住院天数
    var histogramChart4 = Echarts.init(document.getElementById('lineChart'));
    histogramChart4.setOption( {
        color:['#5bc0de'],
        grid:{
            left: '5%',
            right: '5%',
            bottom: '5%',
            containLabel: true
        },
        tooltip : {
            trigger: 'item',
            formatter: "{a}<br/>{b}<br/>{c}公斤"
        },
        calculable : true,
        xAxis : [
            {
                type : 'category',
                data : ['自来水深度处理','污水处理','烟气脱硝','黑臭水体治理',],
                axisLine:{
                    lineStyle:{
                        color: '#87cefa'
                    },
                },
                axisLabel : {
                    interval:0,
                    rotate:40,

                    textStyle: {
                        color: '#fff',
                        fontSize:13
                    }
                }
            }
        ],
        yAxis : [
            {
                type : 'value',
                axisLine:{
                    lineStyle:{
                        color: '#87cefa'
                    },
                },
                splitLine: {
                    "show": false
                },
                axisLabel: {
                    textStyle: {
                        color: '#fff'
                    },
                    formatter: function (value) {
                        return value + "公斤"
                    },
                },
            }
        ],
        series : [
            {
                name:'应用领域',
                type:'bar',
                barWidth:20,
                itemStyle:{
                    color:'#2ab9d8',
                    normal: {
                            //柱形图圆角，初始化效果
                            barBorderRadius:[6, 6, 0, 0],
                            
                        }
                },
                data:[600,800,758,526],
            },
        ]
    });
        }
    }
}
</script>
<style  scoped>
.Mmain{position: relative; width:400px; height: 400px; margin: 0 0 20px;}
   .Mmain>img{ width: 100%; height: 100%;} 
   .Mmain>h3{ position: absolute; top: 0; left: 0; width: 100%; height: 50px;
   line-height: 50px;text-align: center;color: skyblue; font-size: 20px;
   /* background: url('../assets/img/title.png') left center no-repeat; */
   background-size: 100%; z-index: 100;}
    .mycharts{
        width: 400px; height: 400px;
        position: absolute; z-index: 99;
        top:0; left: 0;;
    }
</style>
