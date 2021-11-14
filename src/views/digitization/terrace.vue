<template>
  <div class="terrace">
    <div class="header"></div>
    <div class="mian">
      <div class="left-content">
        <div class="info">
          <h2>村情简介</h2>
          <div class="info-detail">

          </div>
        </div>
        <div class="info">
          <h2>人口情况</h2>
          <annular/>
        </div>
        <div class="info">
          <h2>务工情况</h2>
          <histogram/>
        </div>
      </div>
      <div class="right-content">
        <div class="property">
          <h2>资金管理</h2>
          <div class="property-detail"></div>
        </div>
         <div class="property">
          <h2>乡村产业</h2>
          <dynamic/>
        </div>
      </div>
    </div>
    <div class="footer"></div>
  </div>
</template>

<script>
import annular from './components/annular'
import doughnut from './components/doughnut'
import dynamic from './components/dynamic'
import histogram from './components/histogram'
export default {
  components:{
    annular,
    doughnut,
    dynamic,
    histogram
  }
}
</script>

<style lang="scss" scoped>
.terrace {
  position: relative;
  width: 100%;
  height: 100%;
  background: url('../../assets/img/main_bg.9cb3d9f2.png') no-repeat;
  background-size: 100% 100%;
  .header {
    width: 100%;
    height: 60px;
    background: url('../../assets/img/title_bg.ed91aa7c.png') no-repeat;
    background-size: 100% 100%;
  }
  .mian {
    position: absolute;
    left: 0;
    top: 0;
    padding-top: 60px;
    display: flex;
    justify-content: space-between;
    height: calc(100% - 60px);
    width: 100%;
    .left-content {
      position: relative;
      width: 300px;
      height: 100%;
      padding-left: 40px;
      background: linear-gradient(90deg,rgba(41,82,125,.8),rgba(41,82,125,0));
      &::after {
        position: absolute;
        left: 0;
        top: 0;
        content: '';
        width: 45px;
        height: 100%;
        background: url('../../assets/img/left_right_line.8db324c1.png') no-repeat;
        background-size: 100% 100%;
      }
      .info {
        display: flex;
        flex-direction: column;
        h2 {
          height: 30px;
          background: url('../../assets/img/sub_title_bg_left.a2aa471e.png') no-repeat;
          background-size: 100% 100%;
          color: #fff;
          line-height: 30px;
          padding-left: 30px;
          font-weight: 600;
          font-size: 14px;
        }
        .info-detail {
          width: 100%;
          height: 170px;
          background: url('../../assets/img/sub_content_bg.ba60007b.png') no-repeat;
          background-size: 100% 100%;
          margin: 10px;
        }
      }
      
    }
    .right-content {
      position: relative;
      width: 300px;
      height: 100%;
      padding-left: 40px;
      background: linear-gradient(-90deg,rgba(41,82,125,.8),rgba(41,82,125,0));
      padding-right: 40px;
      &::after {
        position: absolute;
        right: 0;
        top: 0;
        content: '';
        width: 45px;
        height: 100%;
        background: url('../../assets/img/left_right_line.8db324c1.png') no-repeat;
        background-size: 100% 100%;
        transform: scaleX(-1);
      }
      .property {
        display: flex;
        flex-direction: column;
        width: 300px;
        height: 200px;
        h2 {
          height: 30px;
          background: url('../../assets/img/sub_title_bg_right.19d2c3c0.png') no-repeat;
          background-size: 100% 100%;
          color: #fff;
          line-height: 30px;
          padding-left: 30px;
          font-weight: 600;
          font-size: 14px;
          text-align: right;
          padding-right: 30px;
        }
        .property-detail {
          height: 170px;
          width: 100%;
          background: url('../../assets/img/sub_content_bg.ba60007b.png') no-repeat;
          background-size: 100% 100%;
          margin-top: 10px;
        }
      }
    }
  }
}
</style>