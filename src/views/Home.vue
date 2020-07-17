<template>
  <div class="home">
    <van-sticky>
      <van-nav-bar
      title="考核情况"
      right-text="..."
      left-arrow
      @click-left="onClickLeft"
      @click-right="onClickRight"
    />
    </van-sticky>
    222
    <div class="test">
      <div>321</div>
      <div>123</div>
    </div>
    <div class="time-box">
      <van-row>
        <van-col span="8" class="sun-box">终端名字</van-col>
        <van-col span="8" class="sun-box">考核开始时间</van-col>
        <van-col span="8" class="sun-box">日均销量</van-col>
      </van-row>
    </div>
    <div class="hr"></div>
    <div class="search">
    </div>
    <div class="detail-box" v-for="(item, index) in list" :key="index">
      <div class="title-box">
        <div>终端名称限制一下字符14个字符</div>
        <div :class="[ (index+1)%2 ?  'fontPink': 'fontGreen']">25.1张</div>
      </div>
      <div class="time">2019-03-15</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
  @import "../assets/styles/pxDivide2";
  html,body,#app{
    height: 100%;
    background: #F6F6F6 !important;
    color: #4A4A4A;
  }
  .test{
    display: flex;
    justify-content: space-around;
    margin-top: pxD2(36);
    div{
      width: pxD2(330);
      height: pxD2(256);
      background: pink;
      border-radius: pxD2(10);
    }
    div:last-child{
      background: url("../assets/images/left.png") 0 0 no-repeat;
      -webkit-background-size: 100% 100%;
      background-size: 100% 100%;
    }
    div:first-child{
      background: url("../assets/images/right.png") 0 0 no-repeat;
      -webkit-background-size: 100% 100%;
      background-size: 100% 100%;
    }
  }
  .search{
    width: pxD2(692);
    height: pxD2(78);
    background: #f6f6f6;
    margin-top: pxD2(15);
    margin-left: auto;
    margin-right: auto;
    margin-bottom: pxD2(7);
  }
  .time-box{
    margin-top: pxD2(40);
    margin-bottom: pxD2(20);
    font-size: pxD2(24);
    padding: 0 pxD2(26);
    color: #4A4A4A;
    .sun-box:first-child{
      text-align: left;
    }
    .sun-box:nth-child(2){
      text-align: center;
      color: #ff5364;
    }
    .sun-box:last-child{
      text-align: right;
    }
  }
  .hr{
    height: pxD2(20);
    width: 100%;
    background: #f6f6f6;
  }
  .title-box{
    display: flex;
    justify-content: space-between;
    padding: 0 pxD2(26);
    font-size: pxD2(28);
    margin-top: pxD2(33);
    margin-bottom: pxD2(35);
  }
  .fontPink{
    color: #ff2741;
  }
  .fontGreen{
    color: #67da9f;
  }
  .time{
    padding: 0 pxD2(26);
    font-size: pxD2(24);
    color: #666666;
    margin-bottom: pxD2(30);
  }
  .detail-box{
    border-bottom: pxD2(1) solid #e5e5e5;
  }
</style>

<script>
// @ is an alias to /src
import { NavBar, Sticky, Row, Col } from 'vant'
export default {
  name: 'home',
  components: {
    [NavBar.name]: NavBar,
    [Sticky.name]: Sticky,
    [Row.name]: Row,
    [Col.name]: Col
  },
  data () {
    return {
      list: [1, 2, 3, 4, 5, 6]
    }
  },
  methods: {
    onClickLeft () {
      console.log(1)
    },
    onClickRight () {
      console.log(2)
    }
  }
}
</script>
