<template>
<div class="page5" >
    <span unselectable="on" >
    <div class="title">年節親戚聊天專用指南</div>
    
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
      </div>

        <div class="bigitem">年前準備</div>
            <el-progress type="dashboard" :percentage="percentage" :color="colors"></el-progress>
            <div>
            <el-button-group>
                <el-button icon="fa fa-chevron-down" @click="decrease"></el-button>
                <el-button icon="fa fa-chevron-up" @click="increase"></el-button>
            </el-button-group>
            </div>
        <div class="smallitem">
            <a href="https://www.youtube.com/user/TBSCTS">華視 </a>
            <a href="https://www.youtube.com/user/setnews159">三立 </a>
            <a href="https://www.youtube.com/channel/UCBuHkb1AS_yRQ71meFNQ3VQ">年代 </a>
            <a href="https://www.youtube.com/channel/UCp2f7tGJGN6R9Muxipem8Nw">寰宇 </a>
            <a href="https://www.youtube.com/user/NTDAPTV">新唐人 </a>
            <a href="https://www.youtube.com/channel/UCTqPBBnP2T57kmiPQ87986g">眼球中央電視台 </a>
            <a href="https://www.youtube.com/user/twnexttv">壹電視 </a>
            <a href="https://www.youtube.com/channel/UCpu3bemTQwAU8PqM4kJdoEQ">中天</a>
            <a href="https://www.youtube.com/user/TVBS">TVBS </a>
            <a href="https://www.youtube.com/user/newsebc">東森 </a>
            <a href="https://www.youtube.com/user/chinatvnews">中視 </a>
            <a href="https://www.youtube.com/user/ttvnewsview">台視 </a>
            <a href="https://www.youtube.com/user/FTVCP">民視 </a>
            </div>
    
    </span>
</div>
</template>


<script>
  export default {
    data() {
      return {
        percentage: 50,
        colors: [
          {color: 'red', percentage: 20},
        ]
      };
    },
    methods: {
      increase() {
        this.percentage += 2;
        if (this.percentage > 99) {
          this.percentage = 99;
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
    font-family:"normalc"
}
.title{
    padding-top:10vh;
    width:100vw;
    font-size:70px;
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
    font-family:"normalc";
    color:white;
}
.contain{
    font-size:18px;
    text-align: left;
    padding:10px;
    padding-left:10vw;
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
a{
  color:white;
  text-decoration: none;
}
</style>