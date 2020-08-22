<template>
  <div class="home">
    <Top></Top>
    <div class="in_Statistics">
      <div>
        <VProject></VProject>
      </div>
      <div>
        <EquipmentSet></EquipmentSet>
      </div>
      <div>
        <EquipmentKg></EquipmentKg>
      </div>
    </div>
    <div class="icenter">
      <div class="ileft">
        <div class="div01">
          <Cyly></Cyly>
          <Cyqs></Cyqs>
        </div>
      </div>
      <div class="mapdiv">
        <Eqmap></Eqmap>
      </div>
      <div class="iright">
        <Cyfb></Cyfb>
         <Xmfb></Xmfb>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Top from "../components/top"; //头部
import VProject from "../components/project"; //项目
import EquipmentSet from "../components/equipmentSet"; //装备（套）
import EquipmentKg from "../components/equipmentKg"; //装备（公斤）
import Cyly from "../components/cyly"; //臭氧应用领域
import Cyqs from "../components/cyqs"; //臭氧应用趋势
import Eqmap from "../components/eqmap"; //臭氧应用趋势
import Cyfb from "../components/cyfb"; //臭氧用量分布
import Xmfb from "../components/xmfb"; //项目应用分布

export default {
  name: "Home",
  components: {
    Top,
    VProject,
    EquipmentSet,
    EquipmentKg,
    Cyly,
    Cyqs,
    Eqmap,
    Cyfb,
    Xmfb
  },
};
</script>
<style scoped>
.home {
  background: url("../assets/img/top.png") center top no-repeat;
  background-size: 100%;
}
.in_Statistics {
  display: flex;
  height: 148px;
  padding: 0 15px;
}
.in_Statistics > div {
  width: 32.3%;
  margin: 0 0.5%;
}
.icenter{ padding: 15px 20px; display: flex;}
.ileft{ width: 420px;}
.mapdiv{ width: 1050px;}
</style>
