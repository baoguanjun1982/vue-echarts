<template>
    <div class="Mmain">
        <h3>
            臭氧应用领域
        </h3>
         <img src="../assets/img/hor-box-border.png">
        <div id="pieChart1" class="mycharts" >
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
              var pieChart1 = Echarts.init(document.getElementById('pieChart1'));
            pieChart1.setOption({
                color:["#1db190","#0dbbf4","#bbbd0d","#dc5526",],
                tooltip : {
                    trigger: 'item',
                    formatter: "{a}<br/>{b}<br/>{c}个项目"
                },
            calculable : true,
            series : [
                 {
            name: '面积模式',
            type: 'pie',
            radius: [30, 110],
            center: ['46%', '50%'],
            roseType: 'area',
            data:[
                        {value:335, name:'自来水深度处理'},
                        {value:310, name:'污水处理'},
                        {value:234, name:'烟气脱硝'},
                        {value:135, name:'黑臭水体治理'}
                    ]
        }
                // {
                //     name:'应用领域',
                //     type:'pie',
                //     radius : [30, 110],
                //     center : ['50%', '50%'],
                //     roseType : 'area',
                //     x: '50%',
                //     max: 40,
                //     roseType: 'area',
                //     sort : 'ascending',
                //     data:[
                //         {value:335, name:'自来水深度处理'},
                //         {value:310, name:'污水处理'},
                //         {value:234, name:'烟气脱硝'},
                //         {value:135, name:'黑臭水体治理'}
                //     ]
                // }
            ]
        })
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
