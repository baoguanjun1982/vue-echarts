<template>
  <div class="Mmain">
    <h3>
      臭氧应用趋势
    </h3>
    <img src="../assets/img/hor-box-border.png" />
    <div id="histogramChart" class="mycharts"></div>
  </div>
</template>
<script>
import Echarts from "echarts";
export default {
  data() {
    return {};
  },
  mounted() {
    this.getmyechars();
  },
  methods: {
    getmyechars() {
      var lineChart2 = Echarts.init(document.getElementById("histogramChart"));
      lineChart2.setOption({
        // label:{

        // },
        color: ["#1f46c3", "#10a5c5", "#23d27e", "#e5c02a"],
        tooltip: {
          trigger: "item",
          formatter: "{a}<br/>{b}<br/>{c}公斤",
        },
        legend: {
          data: ["自来水", "污水", "烟气", "黑臭水体"],
          y: 60,
          right: 20,
          icon: "roundRect",
          itemWidth: 10,
          itemHeight: 10,
          textStyle: {
            color: "#35ded4",
            fontSize: 12,
          },
        },
        grid: {
          left: "5%",
          right: "5%",
          bottom: "5%",
          top: "30%",
          containLabel: true,
        },
        calculable: true,
        xAxis: [
          {
            type: "category",
            boundaryGap: false,
            data: ["2015年", "2016年", "2017年", "2018年", "2019年"],
            axisLine: {
              lineStyle: {
                color: "#87cefa",
              },
            },
            axisLabel: {
              interval: 0,
              rotate: 40,

              textStyle: {
                color: "#fff",
                fontSize: 13,
              },
            },
          },
        ],
        yAxis: [
          {
            type: "value",
            axisLine: {
              lineStyle: {
                color: "#87cefa",
              },
            },
            splitLine: {
              show: false,
            },
            axisLabel: {
              textStyle: {
                color: "#fff",
              },
              formatter: function(value) {
                return value + "公斤";
              },
            },
          },
        ],
        series: [
          {
            name: "自来水",
            type: "line",
            smooth: true,
            itemStyle: {
              normal: {
                areaStyle : {
							type : 'default',
                            //渐变色实现
						color : new Echarts.graphic.LinearGradient(0, 0, 0, 1,//变化度
                                //三种由深及浅的颜色
									[ {
										offset : 0,
										color : '#1142de'
									}, {
										offset : 0.5,
										color : '#092684'
									}, {
										offset : 1,
										color : '#14323f'
									} ]),
						},
						lineStyle : {  //线的颜色
							color : '#1142de'
						},
                      
                
              },
            },
            data: [221, 524, 460, 530, 610],
          },
          {
            name: "污水",
            type: "line",
            smooth: true,
            itemStyle: {
              normal: {
                areaStyle : {
							type : 'default',
                            //渐变色实现
						color : new Echarts.graphic.LinearGradient(0, 0, 0, 1,//变化度
                                //三种由深及浅的颜色
									[ {
										offset : 0,
										color : '#00d2ff'
									}, {
										offset : 0.5,
										color : '#007791'
									}, {
										offset : 1,
										color : '#01303a'
									} ]),
						},
						lineStyle : {  //线的颜色
							color : '#00d2ff'
						},
                       
                
              },
            },
            data: [534, 691, 490, 130, 110],
          },
          {
            name: "烟气",
            type: "line",
            smooth: true,
             itemStyle: {
              normal: {
                areaStyle : {
							type : 'default',
                            //渐变色实现
						color : new Echarts.graphic.LinearGradient(0, 0, 0, 1,//变化度
                                //三种由深及浅的颜色
									[ {
										offset : 0,
										color : '#23d27e'
									}, {
										offset : 0.5,
										color : '#008c48'
									}, {
										offset : 1,
										color : '#00321a'
									} ]),
						},
						lineStyle : {  //线的颜色
							color : '#23d27e'
						},
                      
						
                
              },
            },
            data: [161, 134, 112, 190, 120],
          },
          {
            name: "黑臭水体",
            type: "line",
            smooth: true,
             itemStyle: {
              normal: {
                areaStyle : {
							type : 'default',
                            //渐变色实现
						color : new Echarts.graphic.LinearGradient(0, 0, 0, 1,//变化度
                                //三种由深及浅的颜色
									[ {
										offset : 0,
										color : '#e5c02a'
									}, {
										offset : 0.5,
										color : '#b28e00'
									}, {
										offset : 1,
										color : '#4c3d00'
									} ]),
						},
						lineStyle : {  //线的颜色
							color : '#e5c02a'
						},
                       
                
              },
            },
            data: [461, 34, 202, 93, 222],
          },
        ],
      });
    },
  },
};
</script>
<style scoped>
.Mmain {
  position: relative;
  width: 400px;
  height: 400px;
}
.Mmain > img {
  width: 100%;
  height: 100%;
}
.Mmain > h3 {
  position: absolute;
  top: 5px;
  left: 0;
  width: 100%;
  height: 50px;
  line-height: 50px;
  text-align: center;
  color: skyblue;
  font-size: 20px;
  /* background: url('../assets/img/title.png') left center no-repeat; */
  background-size: 100%;
  z-index: 100;
}
.mycharts {
  width: 400px;
  height: 400px;
  position: absolute;
  z-index: 99;
  top: 0;
  left: 0;
}
</style>
