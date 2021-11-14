<template>
  <div class="big-screen">
    <div class="header"></div>
    <div class="mian">
      <div class="left-box">
        <div class="conter-box cqgk">
          <div class="conter-title"><span>村情概括</span></div>
          <div class="conter-detail">
            <ul>
              <li>
                <span>外出务工</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>务农</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>务农</span>
                <span><strong>12</strong><i>/户</i></span>
              </li>
              <li>
                <span>贫困人数</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
            </ul>
          </div>
        </div>

        <div class="conter-box dlwz">
          <div class="conter-title"><span>地理位置</span></div>
          <div class="conter-detail">
            <p>道超村位于杨集乡东南部，距乡政府所在地7公里。南靠胡族乡王湖村，西邻余岗村，北邻田湖村，东面与城郊乡接壤。</p>
          </div>
        </div>

        <div class="conter-box jczz">
          <div class="conter-title"><span>基础组织</span></div>
          <div class="conter-detail">
            <ul>
              <li>
                <span>党员人数</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>议事会成员</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>流动党员</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>监委会人员</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>村民代表</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
            </ul>
          </div>
        </div>

        <div class="conter-box dyzc">
          <div class="conter-title"><span>党员组成</span></div>
          <div class="conter-detail">
           <ul>
             <li>
               <span>入库党员</span>
               <div class="progress">
                 <el-progress :percentage="100" :format="'50'"></el-progress>
               </div>
             </li>
             <li>
               <span>入库党员</span>
               <div class="progress">
                 <el-progress :percentage="100" :format="'50'"></el-progress>
               </div>
             </li>
             <li>
               <span>预备党员</span>
               <div class="progress">
                 <el-progress :percentage="100" :format="'50'"></el-progress>
               </div>
             </li>
             <li>
               <span>女性党员</span>
               <div class="progress">
                 <el-progress :percentage="100" :format="'50'"></el-progress>
               </div>
             </li>
             <li>
               <span>少数民族党员</span>
               <div class="progress">
                 <el-progress :percentage="100" :format="'50'"></el-progress>
               </div>
             </li>
             <li>
               <span>大专及以上学历党员</span>
               <div class="progress">
                 <el-progress :percentage="100" :format="'50'"></el-progress>
               </div>
             </li>
           </ul>
          </div>
        </div>
      </div>
      <div class="content-box">
        <div class="content-box-top">
          <div class="contont-list">
            <b>
              <span><strong>12</strong><i>/亩</i></span>
              <span>总面积</span>
            </b>
             <b>
              <span><strong>12</strong><i>/组</i></span>
              <span>户数</span>
            </b>
          </div>
          <div class="contont-list">
            <b>
              <span><strong>12</strong><i>/组</i></span>
              <span>村民组</span>
            </b>
             <b>
              <span><strong>12</strong><i>/人</i></span>
              <span>人数</span>
            </b>
          </div>
        </div>
         <div class="conter-box jczz">
          <div class="conter-title"><span>社会经济状况</span></div>
          <div class="conter-detail">
            <ul>
              <li>
                <span>人口情况</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>议事会成员</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>流动党员</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>监委会人员</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>村民代表</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="right-box">
        <div class="conter-box economics">
          <div class="conter-title"><span>社会经济状况</span></div>
          <div class="conter-detail economics-content">
            <div class="economics-left">
              <div class="economics-echarts">
                <span>主导产业收入</span>
                <div class="economics-ele" id="doughnut"></div>
              </div>
              <div class="farming">
                <span>水稻</span>
                <span>小麦</span>
                <span>有料作物</span>
                <strong><span>1233</span>万元</strong>
              </div>
            </div>
            <div class="economics-right">
              <p>
                <span>工商户</span>
                <strong>21321</strong>
                <i>户</i>
              </p>
              <p>
                <span>经济收入</span>
                <strong>21321</strong>
                <i>元</i>
              </p>
              <p>
                <span>经济收入</span>
                <strong>21321</strong>
                <i>元</i>
              </p>

            </div>
          </div>
        </div>

        <div class="conter-box husbandman">
          <div class="conter-title"><span>百姓关怀</span></div>
          <div class="conter-detail husbandman-content">
            <div class="husbandman-detial">
              <p><span>建档立卡脱贫户</span></p>
              <div class="husbandman-remark">
                <span><strong>3232</strong>户</span>
                <img src="./img/ren.png"/>
                <span><strong>3232</strong>户</span>
              </div>
              <div class="husbandman-conter">
                <div class="husbandman-conter-left">
                  <div class="economics-ele" id="doughnut1"></div>
                  <div class="husbandman-conter-style">
                    <span>已脱贫户（享受政策）</span>
                    <span><strong>121</strong>户</span>
                    <span><strong>121</strong>人</span>
                  </div>
                </div>
                <div class="husbandman-conter-style">
                    <span>已脱贫户（不享受政策）</span>
                    <span><strong>121</strong>户</span>
                    <span><strong>121</strong>人</span>
                  </div>
              </div>
            </div>

            <div class="husbandman-detial" style="margin-top:30px">
              <p><span>三类监测对象户</span></p>
              <div class="husbandman-remark">
                <span><strong>3232</strong>户</span>
                <img src="./img/ren.png"/>
                <span><strong>3232</strong>户</span>
              </div>
              <div class="husbandman-conter">
                <div class="husbandman-conter-left">
                  <div class="economics-ele" id="doughnut1"></div>
                  <div class="husbandman-conter-style">
                    <span>突发严重困难户</span>
                    <span><strong>121</strong>户</span>
                    <span><strong>121</strong>人</span>
                  </div>
                </div>
                <div class="husbandman-conter-style">
                    <span>已消除风险“三类监测对象”</span>
                    <span><strong>121</strong>户</span>
                    <span><strong>121</strong>人</span>
                  </div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import * as echarts from "echarts/core";
export default {
  data() {
    return {};
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      var option = {
        color: ["#00D8FF", "#142641"],
        series: [
          {
            name: 'Access From',
            type: 'pie',
            radius: ['70%', '80%'],
            avoidLabelOverlap: false,
            label: {
              show: false,
              position: 'center'
            },
            emphasis: {
              label: {
                show: true,
                fontSize: '40',
                fontWeight: 'bold'
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 1048, name: '12' },
              { value: 735, name: '123' },
            ]
          }
        ]
      };
      var myChart = echarts.init(document.getElementById("doughnut"));
      myChart.setOption(option);
      var myChart1 = echarts.init(document.getElementById("doughnut1"));
      myChart1.setOption(option);
    },
  },
};
</script>

<style lang="scss" scoped>
.big-screen {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  
  background: url('./img/bg.png') no-repeat center;
  background-color: #041636;
  background-size: 775px 775px;
  .header {
    height: 60px;
    width: 100%;
    background: url('./img/header.png') no-repeat;
    background-size: 100% 100%;
  }
  .mian {
    display: flex;
    padding: 0 20px;
    .left-box {
      width: 600px;
    }
    .content-box {
      width: 600px;
      padding: 0 10px;
    }
  }
}
.conter-box {
  display: flex;
  flex-direction: column;
  width: 100%;
  .conter-title {
    position: relative;
    color: #fff;
    font-size: 24px;
    height: 40px;
    &::after {
      position: absolute;
      bottom: -10px;
      left: 0;
      height: 10px;
      width: 100%;
      content: '';
      display: inline-block;
      background: url('./img/title_bottom.png') no-repeat;
      background-size: 100% 100%;

    }
    span {
      display: inline-block;
      position: relative;
      text-indent: 24px;
      &::after {
        position: absolute;
        top: 5px;
        left: 0;
        content: '';
        display: inline-block;
        width: 14px;
        height: 14px;
        border: 2px solid #65BEFF;
        border-radius: 50%;
        opacity: 1;
      }
    }
  }
  .conter-detail {
    position: relative;
    width: 100%;
    border-left: 1px solid #00D8FF;
    margin-top: 20px;
  }
}
.cqgk {
  ul {
    height: 120px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
    box-sizing: border-box;
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    opacity: 0.65;
    li {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;
      span {
        font-size: 18px;
        font-weight: 500;
        strong {
          color: #00FE90;
          font-size: 40px;
        }
        i {
          font-style: normal;
        }
      }
    }
  }
}
.dlwz {
  display: flex;
  width: 100%;
  margin-top: 20px;
  p {
    display: flex;
    align-items:  center;
    height: 100px;
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    opacity: 0.65;
    color: #fff;
    font-size: 18px;
    padding: 0 30px;
  }
}
.jczz {
  margin-top: 20px;
  ul {
    height: 120px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
    box-sizing: border-box;
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    opacity: 0.65;
    li {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;
      span {
        font-size: 18px;
        font-weight: 500;
        strong {
          color: #00FE90;
          font-size: 40px;
        }
        i {
          font-style: normal;
        }
      }
    }
  }
}
.dyzc {
  margin-top: 30px;
  ul {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    padding: 0 30px;
    li {
      display: flex;
      justify-content: space-between;
      height: 50px;
      span {
        display: inline-block;
        width: 240px;
        color: #fff;
        font-size: 18px;
        padding-left: 28px;
        position: relative;
        &::after {
          content: '';
          position: absolute;
          width: 22px;
          height: 22px;
          left: 0;
          background: url('./img/dan.png') no-repeat;
          background-size: 100% 100% ;
        }
      }
      .progress {
        width: 500px;
      }
    }
  }
}
.content-box-top {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 500px;
  width: 100%;
  .contont-list {
    display: flex;
    justify-content: space-around;
    width: 100%;
    color: #fff;
    padding: 20px;
    box-sizing: border-box;
    b {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 167px;
      height: 118px;
      background: url('./img/content_bg.png') no-repeat;
      background-size: 100% 100%;
      span {
        font-size: 24px;
        strong {
          font-size: 50px;
          color: #00FE90;
          font-weight: 400;
        }
        i {
          font-style: normal;
        }
      }
    }
  }
}
.right-box {
  width: 600px;
}
.economics {
  .economics-content {
    justify-content: space-between;
    .economics-left {
      display: flex;
      
    }
    display: flex;
    .economics-echarts {
      width: 215px;
      height: 215px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      .economics-ele {
        height: 200px;
        width: 200px;
      }
      span {
        color: #fff;
        font-size: 18px;
      }
    }
    .farming {
      display: flex;
      flex-direction: column;
      color: #fff;
      margin-top: 50px;
      span {
        font-size: 18px;
      }
      strong {
        margin-top: 20px;
        color: #00FE90;
        span {
          font-size: 24px;
        }
      }
    }
    .economics-right {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 40px 0;
      box-sizing: border-box;
      p {
        color: #fff;
        span {
          display: inline-block;
          font-size: 18px;
          width: 100px;
        }
        strong {
          display: inline-block;
          font-size: 24px;
          color: #00FE90;
          width: 100px;
        }
      }
    }
  }
}
.husbandman {
  margin-top: 30px;
  .husbandman-content {
    .husbandman-detial {
      box-sizing: border-box;
      padding: 0 30px;
      display: flex;
      flex-direction: column;
      p {
        color: #fff;
        text-align: center;
        font-size: 20px;
        span {
          position: relative;
          &::after {
            position: absolute;
            content: '';
            width: 180px;
            left: -190px;
            top: 12px;
            height: 1px;
            background: #DEDEDE;
          }
          &::before {
            position: absolute;
            content: '';
            width: 180px;
            right: -190px;
            top: 12px;
            height: 1px;
            background: #DEDEDE;
          }
        }
      }
      .husbandman-remark {
        display: flex;
        justify-content: space-around;
        height: 60px;
        border-bottom: 1px solid #DEDEDE;
        span {
          color: #00FE90;
          font-size: 40px;
          
        }
        img {
          height: 50px;
          width: 50px;
        }
      }
      .husbandman-conter {
        height: 120px;
        display: flex;
        justify-content: space-between;
        padding: 10px;
        
        .husbandman-conter-left {
          display: flex;
          .economics-ele {
            width: 110px;
            height: 110px;
          }
        }
        .husbandman-conter-style {
          display: flex;
          flex-direction: column;
          justify-content: space-around;
          color: #fff;
          span {
            font-size: 18px;
            strong {
              font-size: 30px;
              color: #00FE90;
              display: inline-block;
              width: 100px;
            }
          }
        }
      }
    }
  }
}
</style>