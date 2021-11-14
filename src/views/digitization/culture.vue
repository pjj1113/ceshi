<template>
  <div class="culture">
    <div class="header">
      <span>数字菌园可视化</span>
    </div>
    <div class="main">
      <div class="left">
        <div class="left-box">
          <h3>基础信息</h3>
          <div class="info-detail">
            <div class="box-01-item">
              <img src="../../assets/img/icon0.ba91cda6.png"/>
              <span>基地数量</span>
              <p>12</p>
            </div>
            <div class="box-01-item">
              <img src="../../assets/img/icon0.ba91cda6.png"/>
              <span>产品种类</span>
              <p>12</p>
            </div>
            <div class="box-01-item">
              <img src="../../assets/img/icon0.ba91cda6.png"/>
              <span>总面积</span>
              <p>12</p>
            </div>
          </div>
        </div>

        <div class="left-box">
          <h3>价格走势</h3>
          <div class="info-detail">
           <Price/>
          </div>
        </div>

        <div class="left-box">
          <h3>区域销售</h3>
          <div class="info-detail">
            <histogram/>
          </div>
        </div>
      </div>
      <div class="mian-conter">
        <China/>
      </div>
      <div class="left">
        <div class="left-box">
          <h3>环境监测</h3>
          <div class="info-detail">
            <ul>
              <li>
                <span>菌棒温度</span>
                <strong>-70.0 ℃</strong>
              </li>
              <li>
                <span>菌棒温度</span>
                <strong>-70.0 ℃</strong>
              </li>
              <li>
                <span>菌棒温度</span>
                <strong>-70.0 ℃</strong>
              </li>
              <li>
                <span>菌棒温度</span>
                <strong>-70.0 ℃</strong>
              </li>
              <li>
                <span>菌棒温度</span>
                <strong>-70.0 ℃</strong>
              </li>
            </ul>
          </div>
        </div>
        <div class="left-box">
          <h3>环境采集</h3>
          <div class="info-detail">
            <histogram/>
          </div>
        </div>
        <div class="left-box">
          <h3>农情预警</h3>
          <ul class="warning-list">
            <li style="background:rgba(20,94,142,.2)">
              <el-row>
                <el-col :span="6">预警类</el-col>
                <el-col :span="4">位置</el-col>
                <el-col :span="4">处置</el-col>
                <el-col :span="8">说明</el-col>
              </el-row>
            </li>
            <li></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Price from './components/price.vue'
import histogram from './components/histogram.vue'
import China from './components/china.vue'
export default {
  components: {
    Price,
    histogram,
    China
  }
}
</script>

<style lang="scss" scoped>
.culture {
  width: 100%;
  height: 100%;
  background: #0e244b;
  overflow: hidden;
  .header {
    text-align: center;
    width: 100%;
    height: 50px;
    line-height: 50px;
    background: url('../../assets/img/bigtitlebg.1fa01ddb.png') no-repeat;
    background-size: 100% 100%;
    span {
      font-size: 24px;
      color: #fff;
    }
  }
  .main {
    display: flex;
    justify-content: space-between;
    height: calc(100%-50px);
    width: 100%;
    box-sizing: border-box;
    padding: 10px;
    .left {
      width: 300px;
      height: 100%;
      .left-box {
        display: flex;
        flex-direction: column;
        margin-bottom: 10px;
        h3 {
          height: 30px;
          width: 100%;
          background: url('../../assets/img/titlebg.d47c2b90.png') no-repeat;
          background-size: 100% 100%;
          box-sizing: border-box;
          color: #fff;
          padding-left: 30px;
          font-size: 16px;
          font-weight: 500;
          margin-bottom: 10px;
        }
        .info-detail {
          display: flex;
          justify-content: space-around;
          // padding-top: .104167rem;
          box-shadow: inset 0 0 5px 5px hsla(0deg,0%,100%,0.18);
          // box-shadow: inset 0 0 0.104167rem 0.03125rem rgba(0,0,255,0.18);
          border: .005208rem solid hsla(0,0%,100%,.3);
          // box-shadow: inset -2px 2px 2px rgba(255,255,255,0.18), inset -2px -2px 2px rgba(255,255,255,0.18), inset 2px -2px 2px rgba(255,255,255,0.18), inset 2px 2px 2px rgba(255,255,255,0.18);
          height: 170px;
          box-sizing: border-box;
          padding: 10px;
          .box-01-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-around;
            img {
              width: 50px;
              height: 50px;
            }
            span {
              color: #fff;
              font-size: 16px;
            }
            p {
              display: flex;
              justify-content: center;
              align-items: center;
              color: #fff;
              font-size: 18px;
              height: 50px;
              width: 100%;
              background: url('../../assets/img/numbg.2ea74974.png') no-repeat;
              background-size: 100% 100%;
            }
          }
          ul {
            display: flex;
            flex-wrap: wrap;
            padding: 3px;
            li {
              position: relative;
              width: 80px;
              height: 60px;
              margin-right: 10px;
              display: flex;
              flex-direction: column;
              justify-content: space-around;
              align-items: center;
              span {
                color: #fff;
              }
              strong {
                color: #03fbfe;
              }
              &::after {
                position: absolute;
                left: 0;
                top: 0;
                content: '';
                background: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAQAAAA2BAMAAAASbSXrAAAAElBMVEUAAAAC+v8C+/8D+/4D+/8D+/4ORTJwAAAABXRSTlMAZn+ysnAXn5kAAAAgSURBVAjXYwgNYghVYAhiYHBgYBAYNMiAAeQkoMNCgwD7NwYtxODh/wAAAABJRU5ErkJggg==') no-repeat;
                background-size: 100% 100%;
                height: 100%;
                width: 3px;
              }
              &::before {
                position: absolute;
                right: 0;
                top: 0;
                content: '';
                background: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAQAAAA2CAYAAADgQzjYAAAARElEQVQ4T2Nk+v2/npHhfwMDFDCCaGRBsACyIFwAJMj8+/8mFAGmX//TRgVgYcbAMBoeIzk5MP/+h8gesFyFmcXQMyEATAGK5PODU1EAAAAASUVORK5CYII=') no-repeat;
                background-size: 100% 100%;
                height: 100%;
                width: 3px;
              }
            }
          }
        }
        .warning-list {
          display: flex;
          flex-direction: column;
          li {
            color: #fff;
          }
        }
      }
    }
    .mian-conter {
      width: calc(100% - 600px);
    }
    .right {
      width: 300px;
      height: 100%;
    }
  }
}
</style>