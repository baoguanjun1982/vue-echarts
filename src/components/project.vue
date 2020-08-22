<template>
  <div class="maindiv">
    <div>
        <i class="el-icon-folder-opened"></i>
      <p>项目总数(个)</p>
      <h3>{{ promun }}</h3>
    </div>
    <div>
        <i class="el-icon-folder-checked"></i>
      <p>
        完成项目数(个)
      </p>
      <h3>{{ promunComplete }}</h3>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      promun: 1235,
      promunComplete: 235,
    };
  },
};
</script>
<style scoped>
.maindiv{
    color:#00c6ff;
    display: flex;
    font-size: 16px;
    background:rgba(0, 194, 250, 0.3);
    padding: 30px 20px;
    border-radius: 10px;
}
.maindiv>div{ width: 30%; position: relative; padding: 0 0 0 20%;}
.maindiv>div>p{ line-height: 22px;}
.maindiv>div>h3{ font-size: 50px; color: #ffff43; font-family:'方正大黑简体';}
.maindiv>div i{ position: absolute; left: 10px; font-size: 40px; top:0px; color: #00c6ff;
 background:rgba(0, 194, 250, 0.3);border-radius: 40px;padding: 15px;
 box-shadow: -10px 0px 15px #034c6a inset, 0px -10px 15px #034c6a inset,
    10px 0px 15px #034c6a inset, 0px 10px 15px #034c6a inset;
    border: 1px solid #00c6ff;
    animation:mymove 2s infinite;}
    @keyframes mymove
    {
    0%   {top:0px;}
    50%  {top:20px;}
    100% {top:0px;}
    }
</style>
