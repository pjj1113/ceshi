<template>
  <div class="big-screen">
    <div class="header"></div>
    <div class="mian">
      <div class="left-box">
        <div class="conter-box education">
          <div class="conter-title"><span>教育设施</span></div>
          <div class="conter-detail education-content">
            <ul>
              <li>
                <span>小学数量</span>
                <span><strong>12</strong><i>/所</i></span>
              </li>
              <li>
                <span>教师数量</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>在校学生</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>学龄儿童</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
            </ul>
            <div class="education-probability">
              <img src="./img/jiaoyu.png"/>
              <div class="jindu">
                <span>学龄儿童入学率</span>
                <i></i>
              </div>
              <span>100%</span>
            </div>
          </div>
        </div>

        <div class="conter-box education" style="margin-top:30px">
          <div class="conter-title"><span>医疗设施</span></div>
          <div class="conter-detail education-content">
            <ul>
              <li>
                <span>村卫生室</span>
                <span><strong>12</strong><i>/间</i></span>
              </li>
              <li>
                <span>从业医生</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
              <li>
                <span>参加新型农村合作医疗人数</span>
                <span><strong>12</strong><i>/人</i></span>
              </li>
            </ul>
            <div class="education-probability">
              <img src="./img/yiliao.png"/>
              <div class="jindu">
                <span>参合率</span>
                <i></i>
              </div>
              <span>100%</span>
            </div>
          </div>
        </div>

        <div class="conter-box aged" style="margin-top:30px">
          <div class="conter-title"><span>养老设施</span></div>
          <div class="conter-detail aged-content">
            <div class="aged-content-left">
              <img src="./img/yanglao.png"/>
              <span>
                <i>参加养老保险人数</i>
                <strong>1243</strong>
              </span>
            </div>
            <div class="baoxian" id="doughnut"></div>
          </div>
        </div>
      </div>
      <div class="content-box">
        <div class="content-box-top">
          <div class="contont-list">
            <b>
              <span><strong>100%</strong></span>
              <span>农网改造率</span>
              <img src="./img/chengshi.png"/>
            </b>
             
          </div>
          <div class="contont-list">
            <b>
              <span><strong>8</strong><i>/M</i></span>
              <span>网络已开通宽带</span>
              <img src="./img/chengshi.png"/>
            </b>
            <b>
              <span><strong>12</strong><i>/组</i></span>
              <span>有线电视数字电视开通率</span>
              <img src="./img/chengshi.png"/>
            </b>
          </div>
        </div>

        <div class="conter-box hdcs">
          <div class="conter-title"><span>活动场所</span></div>
          <div class="conter-detail">
            <p>道超村活动场所位于道超村孙圩组，主用房屋为共十五间一层结构楼房建筑面积 <span>123</span>平方米</p>
            <div class="hdcs-content">
              <div class="hdcs-list">
                <span>党员活动室<strong>3</strong>间</span>
                <span>村两委办公室<strong>3</strong>间</span>
              </div>
              <div class="hdcs-list">
                <span>扶贫办公室<strong>4</strong>间</span>
                <span>大会议室<strong>4</strong>间</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="right-box">

        <div class="conter-box jtss" style="margin-top:30px">
          <div class="conter-title"><span>交通设施</span></div>
          <div class="conter-detail jtss-content">
            <div class="jiaotong" id="doughnut1"></div>
            <div class="lu-list">
              <p><i></i><span>道路总数</span><strong>12</strong><b>公里</b></p>
              <p><i></i><span>水泥硬化</span><strong>12</strong><b>公里</b></p>
              <p><i></i><span>沙石硬化路</span><strong>12</strong><b>公里</b></p>
              <p><i></i><span>通组土路</span><strong>12</strong><b>公里</b></p>
            </div>
          </div>
        </div>   

        <div class="conter-box irrigation-conservancy" style="margin-top:30px">
          <div class="conter-title"><span>农田水利设施</span></div>
          <div class="conter-detail irrigation-conservancy-content">
            <p><span>水塘数量</span><strong>12</strong><i>口</i></p>
            <p><span>沟渠数</span><strong>12</strong><i>条</i></p>
            <p><span>沟渠总长度</span><strong>12</strong><i>公里</i></p>
            <div class="zilaishui"><b>自来水覆盖率</b><div class="jindutiao"></div><strong>12</strong></div>
          </div>
        </div>  

        <div class="conter-box jtss" style="margin-top:30px">
          <div class="conter-title"><span>能源设施</span></div>
          <div class="conter-detail jtss-content">
            <div class="jiaotong" id="doughnut2"></div>
            <div class="lu-list">
              <p><i></i><span>主要燃料</span></p>
              <p><i></i><span>柴草</span><strong>12</strong></p>
              <p><i></i><span>煤气</span><strong>12</strong></p>
              <p><i></i><span>电</span><strong>12</strong></p>
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
      var option1 = {
        color: ["#0045FF", "#008A20","#00D8FF"],
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
              { value: 735, name: '124' },
            ]
          }
        ]
      };
      var myChart = echarts.init(document.getElementById("doughnut"));
      myChart.setOption(option);
      var myChart1 = echarts.init(document.getElementById("doughnut1"));
      myChart1.setOption(option1);

       var myChart2 = echarts.init(document.getElementById("doughnut2"));
      myChart2.setOption(option1);
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
      padding: 0 30px;
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
.education-content {
  background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
  ul {
    height: 120px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
    box-sizing: border-box;
    
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
  .education-probability {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    align-items: center;
    img {
      width: 65px;
      height: 65px;
    }
    span {
      font-size: 35px;
      color: #00FE90;
      font-weight: 600;
      margin-left: 20px;
    }
    .jindu {
      display: flex;
      flex-direction: column;
      margin-left: 30px;

      span {
        color: #fff;
        font-size: 18px;
        margin-left: 0px;
        line-height: 40px;
      }
      i {
        display: inline-block;
        width: 327px;
        height: 6px;
        background: #00D8FF;
      }
    }
  }
}

.aged {
  .aged-content {
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 160px;
    padding:  30px;
    box-sizing: border-box;
    .aged-content-left {
      display: flex;
      align-items: center;
      height: 100%;
      img {
        width: 65px;
        height: 65px;
      }
      span {
        display: flex;
        flex-direction: column;
        color: #fff;
        font-size: 20px;
        padding-left: 30px;
        i {
          font-style: normal;
        }
        strong {
          
          font-size: 40px;
          color: #00FE90;
        }
      }
    }
    .baoxian {
      width: 110px;
      height: 110px;
    }
  }
}

.content-box-top {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 650px;
  width: 100%;
  .contont-list {
    display: flex;
    justify-content: space-around;
    width: 100%;
    color: #fff;
    padding: 20px;
    box-sizing: border-box;
    margin-bottom: 40px;
    b {
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 167px;
      height: 118px;
      background: url('./img/content_bg.png') no-repeat;
      background-size: 100% 100%;
      span {
        font-size: 20px;
        text-align: center;
        strong {
          font-size: 50px;
          color: #00FE90;
          font-weight: 400;
        }
        i {
          font-style: normal;
        }
      }
      img {
        position: absolute;
        left: -90px;
        width: 103px;
        height: 162px;
      }
    }
  }
}
.hdcs {
  p {
    font-size: 20px;
    color: #fff;
    padding: 20px;
    span {
      color: #00FE90;
      font-size: 30px;
      padding: 0 20px;
    }
  }
  .hdcs-content {
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    .hdcs-list {
      display: flex;
      flex-direction: column;
      font-size: 20px;
      color: #fff;
      border-left: 1px solid #00D8FF;
      padding-left: 30px;
      span {
        strong {
          display: inline-block;
          margin-left: 30px;
          margin-right: 30px;
          font-size: 35px;
          color: #00FE90;
        }
      }
    }
  }
}


.right-box {
  width: 600px;
}
.jtss {
  .jtss-content {
    display: flex;
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    height: 215px;
    .jiaotong {
      height: 200px;
      width: 200px;
      margin-left: 50px;
    }
    .lu-list {
      display: flex;
      flex-direction: column;
      p {
        i{
          width: 23px;
          height: 12px;
          background: #008A20;
        }
        span {
          color: #fff;
          font-size: 18px;
          width: 100px;
          display: inline-block;
        }
        strong {
          font-size: 30px;
          color: #00FE90;
          display: inline-block;
          min-width: 80px;
        }
        b {
          color: #fff;
          font-size: 18px;
        }
      }
    }
  }
}

.irrigation-conservancy {
  .irrigation-conservancy-content {
    display: flex;
    flex-direction: column;
    padding: 30px;
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    p {
      display: flex;
      align-items: center;
      margin-bottom: 20px;
      span {
        display: inline-block;
        width: 417px;
        height: 29px;
        background: rgba(0, 216, 255, 0.5);
        font-size: 18px;
        line-height: 29px;
        color: #fff;
        box-sizing: border-box;
        padding: 0 10px;
      }
      strong {
        font-size: 30px;
        color: #00FE90;
        margin-left: 20px;
      }
      i {
        color: #fff;
        font-size: 18px;
        font-style: normal;
        margin-left: 20px;
      }
      
    }
    .zilaishui {
      b {
        font-size: 18px;
        color: #fff;
      }
      strong {
        font-size: 30px;
        color: #00FE90;
        margin-left: 20px;
      }
      .jindutiao {
        width: 254px;
        height: 6px;
        background: #00D8FF;
        display: inline-block;
        margin: 0 30px;
      }
    }
  }
}
</style>