<template>
  <div class="container">
    <div class="imglist">
      <h3>图片列表区</h3>
      <img src="./assets/01.png" alt="" @mouseenter="mouseenter(1)" @click="clickFn(1,$event)">
      <img src="./assets/02.png" alt="" @mouseenter="mouseenter(2)" @click="clickFn(2,$event)">
      <img src="./assets/03.png" alt="" @mouseenter="mouseenter(3)" @click="clickFn(3,$event)">
    </div>
    <div class="show">
      <h3>图片预览区</h3>
      <img :src="currentImg" alt="" style="width:600px;height:auto;">
    </div>
   <div>
   </div>
  </div>
</template>

<script>
import img01 from './assets/01.png'
import img02 from './assets/02.png'
import img03 from './assets/03.png'
export default {
  data() {
    return {
      currentImg:img01
    }
  },
  methods:{
    mouseenter(val){
      this.currentImg = {1:img01,2:img02,3:img03}[val]
    },
    clickFn(n,e){
      alert(`当前是第${n}张，路径是${e.target.src}`)
    }
  }
};
</script>

<style scoped>
  .container {
    display:flex;
  }
 .imglist { 
  border: 2px solid red;
 }
.imglist img {
  width: 200px;
  height: auto;
}
.show {
  border: 2px solid red;
  margin-right: 20px;
}

</style>