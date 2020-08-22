<template>
  <div class="topmain">
    <div class="top">
      大数据展示
    </div>
    <div class="nav">
      <a href="" :class="{nav_active:idex==1}" >设备概况</a>
      <a href="">指标分析</a>
      <a href="">趋势分析</a>
    </div>
  </div>
</template>
<script>
export default {
    data(){
        return{
            idex:1
        }
    }
};
</script>
<style scoped>
.topmain {
  height: 90px;
}
.top {
  line-height: 60px;
  text-align: center;
  font-size: 40px;
  color: #fff;
  letter-spacing:10px;
  font-family: "SimHei";
  font-weight: bold;
}
.nav {
  position: absolute;
  top: 35px;
  left: 10px;
  display: flex;
}
.nav a {
  width: 100px;
  height: 40px;
  line-height: 40px;
  font-size: 18px;
  display: block;
  text-align: center;
  color: #31ced8;
  border-radius: 10px;
  margin: 0 0 0 10px;
   box-shadow: -10px 0px 15px #034c6a inset, 0px -10px 15px #034c6a inset,
    10px 0px 15px #034c6a inset, 0px 10px 15px #034c6a inset;
    
}
.nav_active,.nav a:hover {
  border-bottom: 4px solid #4b8df8;
  box-sizing: border-box;
}
</style>
