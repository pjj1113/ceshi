<template>
  <div class="big-screen">
    <div class="header"></div>
    <div class="mian">
      <div class="top-box">
        <div class="conter-box ganbu" style="width:600px">
          <div class="conter-title"><span>包村干部</span></div>
          <div class="conter-detail ganbu-content">
            <ul class="ganbu-list">
              <li>
                <span>帮扶领导</span>
                <img src=""/>
                <strong>李春（乡纪委书记）</strong>
              </li>
              <li>
                <span>包村干部</span>
                <img src=""/>
                <strong>孙宝印（杨集乡政府科员）</strong>
              </li>
            </ul>
          </div>
        </div>

        <div class="conter-box ganbu" style="width:900px">
          <div class="conter-title"><span>村两委负责人</span></div>
          <div class="conter-detail ganbu-content">
            <ul class="ganbu-list">
              <li>
                <span>村党支部书记</span>
                <img src=""/>
                <strong>余道文</strong>
              </li>
              <li>
                <span>村委会文书</span>
                <img src=""/>
                <strong>张晶</strong>
              </li>
              <li>
                <span>村党支部副书记</span>
                <img src=""/>
                <strong>余学龙</strong>
              </li>
            </ul>
          </div>
        </div>

      </div>
      <div class="botton-box">
        <div class="conter-box ganbu" style="width:900px">
          <div class="conter-title"><span>驻村工作队成员</span></div>
          <div class="conter-detail ganbu-content">
            <ul class="ganbu-list">
              <li>
                <span>驻村队长</span>
                <img src=""/>
                <strong>张宏伟（县移动公司综合部经理）</strong>
              </li>
              <li>
                <span>驻村队员</span>
                <img src=""/>
                <strong>闫昌林（县移动公司中层干部）</strong>
              </li>
              <li>
                <span></span>
                <img src=""/>
                <strong>马腾（县移动公司中层干部）</strong>
              </li>
            </ul>
          </div>
        </div>

        <div class="conter-box ganbu" style="width:600px">
          <div class="conter-title"><span>包村乡直单位帮扶组人员</span></div>
          <div class="conter-detail ganbu-content">
            <ul class="ganbu-list">
              <li>
                <span>包村乡直单位帮扶组队长</span>
                <img src=""/>
                <strong>孙华建（乡农业中心主任）</strong>
              </li>
              <li>
                <span>包村乡直单位帮扶组队员</span>
                <img src=""/>
                <strong>刘刚（乡农业中心副主任）</strong>
              </li>
            </ul>
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
    flex-direction: column;
    padding: 0 20px;
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
.top-box {
  width: 100%;
  display: flex;
  justify-content: space-around;
}
.botton-box {
  width: 100%;
  display: flex;
  justify-content: space-around;
  margin-top: 50px;
}
.ganbu {
  .ganbu-content {
    height: 378px;
    background: linear-gradient(90deg, rgba(1, 7, 21, 0.9) 0%, rgba(1, 10, 23, 0.6) 100%);
    .ganbu-list {
      display: flex;
      justify-content: space-around;
      align-items: center;
      li {
        display: flex;
        flex-direction: column;
        color: #fff;
        span {
          display: inline-block;
          margin-bottom: 20px;
          font-size: 20px;
          line-height: 40px;
        }
        img {
          width: 183px;
          height: 219px;
          background: #566174;
        }
        strong {
          display: inline-block;
          margin-top: 20px;
          font-size: 20px;
          line-height: 40px;

        };
      }
    }
  }
}
</style>