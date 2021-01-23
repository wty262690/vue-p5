<template>
<div class="page5" >
    <span unselectable="on" >
    <div class="title">過年親戚聊天專用指南</div>
    
    <div class="contain">
        <div class="bigitem ">話題預測</div>
        <div class="item">CVOID19</div>
        <div class="item">政治</div>
        <div class="item">股票</div>
        <div class="item">房市</div>
        <div class="item">工作</div>
        <div class="item">學校</div>
        <div class="item">婚嫁</div>
        <i class="fa fa-plus" aria-hidden="true"></i>
        <div class="bigitem">年前準備</div>
        <div class="smallitem">華視 年代 寰宇 新唐人 眼球 壹電視 中天 三立 TVBS 東森 中視 台視 民視</div>
    </div>
    <el-progress type="dashboard" :percentage="percentage" :color="colors"></el-progress>
    <div>
    <el-button-group>
        <el-button icon="fa fa-chevron-down" @click="decrease"></el-button>
        <el-button icon="fa fa-chevron-up" @click="increase"></el-button>
    </el-button-group>
    </div>
    </span>
</div>
</template>


<script>
  export default {
    data() {
      return {
        percentage: 2,
        colors: [
          {color: 'pink', percentage: 20},
          {color: 'yellow', percentage: 40},
          {color: '#5cb87a', percentage: 60},
          {color: '#1989fa', percentage: 80},
          {color: '#6f7ad3', percentage: 100}
        ]
      };
    },
    methods: {
      increase() {
        this.percentage += 2;
        if (this.percentage > 100) {
          this.percentage = 100;
        }
      },
      decrease() {
        this.percentage -= 2;
        if (this.percentage < 0) {
          this.percentage = 0;
        }
      }
    },
  }
</script>





<style scoped>
.page5{
    color:rgb(213, 228, 148);
    font-size:30px;
    position:relative;
    z-index: 2;
}
.title{
    font-size:60px;
    font-family:"cat";
}
.smallitem{
    font-size:20px;
}
.item{
    color:white;
}
.bigitem{
    font-size:30px;
    font-family:"cat";
    color:red;
}
.contain{
    font-size:18px;
    text-align: left;
    padding:10px;
}
.el-button{
  color:white;
  background-color:rgba(0, 0, 0, 0);
  border:0;
  padding:9px ;
}
.el-progress__text{
  color:white;
  font-family:"english";
  letter-spacing: 5px;
}
</style>