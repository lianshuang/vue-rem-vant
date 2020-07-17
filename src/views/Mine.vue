<template>
    <div class="mine">
      222
      <nav-bar :title="title" @navLeft="navleft" @navRight="navRight"></nav-bar>
      <div class="header">
        <div class="ava-box">
          <div class="ava"></div>
          <div class="name-box">
            <div>
              <div class="name">tb提拉米苏4582</div>
              <div class="id">ID:1234567</div>
              <div class="code">赏金码</div>
            </div>
            <div>
              <div class="shopkeeper">店主</div>
              <div class="update">更新资料</div>
            </div>
          </div>
          <div class="money-box"></div>
        </div>
      </div>
      <div class="ad-box">
        <div class="ad">23213</div>
      </div>
      <van-cell-group class="lianmeng">
        <van-cell title="商家联盟专享" is-link value="即将到账233.33元" />
      </van-cell-group>
      <div class="shouyi-box"></div>
      <van-cell-group>
        <van-cell title="我的订单" is-link value="查看全部订单" />
      </van-cell-group>
      <van-grid :column-num="5" :border="false" :clickable="true">
        <van-grid-item icon="photo-o" text="文字" />
        <van-grid-item icon="photo-o" text="文字" />
        <van-grid-item icon="photo-o" text="文字" />
        <van-grid-item icon="photo-o" text="文字" />
        <van-grid-item icon="photo-o" text="文字" />
      </van-grid>
    </div>
</template>

<script>
import NavBar from '../components/Navbar'
import { Cell, CellGroup, GridItem, Grid } from 'vant'
export default {
  name: 'mine',
  components: {
    [Cell.name]: Cell,
    [CellGroup.name]: CellGroup,
    [GridItem.name]: GridItem,
    [Grid.name]: Grid,
    NavBar
  },
  data () {
    return {
      title: '店促通'
    }
  },
  methods: {
    navleft () {
      console.log(`nabLeft`)
    },
    navRight () {
      console.log(`navRight`)
    }
  }
}
</script>

<style scoped lang="scss">
  @import "../assets/styles/pxDivide2";
  .mine{
    background: #f6f6f6;
  }
  .header{
    width: 100%;
    height: pxD2(258);
    background: #ff2741;
    padding-top: pxD2(36);
    position: relative;
    .ava-box{
      font-size: pxD2(24);
      /*margin-top: pxD2(36);*/
      display: flex;
      margin-left: pxD2(30);
      .ava{
        width: pxD2(83);
        height: pxD2(83);
        border-radius: 50%;
        background: #fff;
      }
      .name-box{
        margin-left: pxD2(13);
      }
      .name-box div:first-child{
        display: flex;
        .name{
          font-size: pxD2(28);
          color: #fff;
        }
        .id{
          font-size: pxD2(24);
          color: #ffbdc2;
          margin-left: pxD2(14);
        }
        .code{
          width: pxD2(98);
          height: pxD2(31);
          background: #ffdf80;
          border-radius: pxD2(10);
          text-align: center;
          margin-left: pxD2(115);
          font-size: pxD2(22);
          line-height: pxD2(31);
          color: #f55a05;
        }
      }
      .name-box div:last-child{
        display: flex;
        color: #ffc30e;
        /*margin-top: pxD2(20);*/
        .shopkeeper{
          margin-top: pxD2(20);
          margin-right: pxD2(20);
          width: pxD2(95);
          height: pxD2(30);
          line-height: pxD2(30);
          border-radius: pxD2(10);
          background: #f8102c;
        }
        .update{
          margin-top: pxD2(20);
          /*padding: pxD2(7) pxD2(10);*/
          width: pxD2(120);
          height: pxD2(30);
          background: #f8102c;
        }
      }
    }
    .money-box{
      width: pxD2(690);
      height: pxD2(142);
      background: #000;
      position: absolute;
      border-radius: pxD2(10);
      left: 50%;
      transform: translateX(-50%);
      bottom: pxD2(-45);
    }
  }
  .shopkeeper{
    text-align: center;
  }
  .update{
    text-align: center;
  }
  .code{
    text-align: center;
  }
  .ad-box{
    width: 100%;
    height: pxD2(204);
    /*height: 204px;*/
    background: pink;
    padding-top: pxD2(70);
    .ad{
      width: pxD2(690);
      height: pxD2(122);
      border-radius: pxD2(80);
      margin-left: auto;
      margin-right: auto;
      background: greenyellow;
      /*margin-top: pxD2(70);*/
    }
  }
  .shouyi-box{
    width: 100%;
    height: pxD2(500);
    background: #f6f6f6;
  }
  .lianmeng{
    margin-top: pxD2(20);
  }
  /*继承写法*/
  .font{
    font-size: pxD2(28);
    color: pink;
  }
  .ad{
    @extend .font;
    text-align: center;
  }
</style>
