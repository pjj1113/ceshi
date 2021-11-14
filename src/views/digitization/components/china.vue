<template>
  <div class="china">
    <div class="china-top">
      <div class="map-bg"></div>
      <div id="mapChart" class="chart"></div>
    </div>
  </div>
</template>
<script>
import * as echarts from "echarts/core";
import axios from "axios";
export default {
  props: {},
  data() {
    return {
      mapOption: {
        titleColor: "pink",
      },
      mapData: [
        {
          flight_ids: "11,18,24",
          from: "保山",
          from_longitude: "99.1729",
          from_latitude: "25.05753",
          to: "南昌",
          to_longitude: "115.9000015258789",
          to_latitude: "28.864999771118164",
          num: 483,
        },

        
        {
          flight_ids: "9,14,21,27",
          from: "南昌",
          from_longitude: "115.9000015258789",
          from_latitude: "28.864999771118164",
          to: "珠海",
          to_longitude: "113.375999",
          to_latitude: "22.006399",
          num: 124,
        },
        {
          flight_ids: 28,
          from: "昆明",
          from_longitude: "102.9291667",
          from_latitude: "25.1019444",
          to: "成都",
          to_longitude: "103.9469985961914",
          to_latitude: "30.578500747680664",
          num: 10,
        },
        {
          flight_ids: 29,
          from: "南京",
          from_longitude: "118.86199951171875",
          from_latitude: "31.742000579833984",
          to: "昆明",
          to_longitude: "102.9291667",
          to_latitude: "25.1019444",
          num: 40,
        },
        {
          flight_ids: 92,
          from: "南京",
          from_longitude: "118.86199951171875",
          from_latitude: "31.742000579833984",
          to: "保山",
          to_longitude: "99.1729",
          to_latitude: "25.05753",
          num: 13,
        },
        {
          flight_ids: 93,
          from: "南京",
          from_longitude: "118.86199951171875",
          from_latitude: "31.742000579833984",
          to: "呼和浩特",
          to_longitude: "111.823997498",
          to_latitude: "40.851398468",
          num: 208,
        },
      ],
    };
  },
  computed: {
    // 通过计算值，将mapOption的默认值补全
    chartOption() {
      return {
        titleColor: "#8796B000",
        backgroundColor: "#2B364800",
        areaColor: "#262C38",
        borderColor: "#678EE3",
        hoverAreaColor: "#16467B",
        lineColor: "rgb(192, 158, 255)",
        trailColor: "#fff",
        endColor: "rgb(192, 158, 255)",
        ...this.mapOption,
      };
    },
  },
  methods: {
    mapChart() {
      axios.get("/static/json/map/100000.json", {}).then((response) => {
        console.log(response)
        var chinaJson = response.data;
        echarts.registerMap("china", chinaJson);
        var series = [];
        series.push(
          {
            type: "lines",
            zlevel: 1,
            effect: {
              show: true,
              period: 6,
              trailLength: 0.7,
              color: this.chartOption.trailColor,
              symbolSize: 3,
            },
            lineStyle: {
              normal: {
                width: 0,
                curveness: 0.2,
              },
            },
            data: this.initData1(this.mapData),
          },
          {
            type: "lines",
            zlevel: 2,
            effect: {
              show: true,
              period: 6,
              trailLength: 0,
              symbolSize: 5,
            },
            lineStyle: {
              normal: {
                color: this.chartOption.lineColor,
                width: 1,
                opacity: 0.4,
                curveness: 0.2,
              },
            },
            data: this.initData1(this.mapData),
          },
          {
            type: "effectScatter",
            coordinateSystem: "geo",
            zlevel: 2,
            rippleEffect: {
              brushType: "stroke",
            },
            label: {
              normal: {
                show: true,
                position: "right",
                formatter: "{b}",
              },
            },
            symbolSize: function (val) {
              return val[2] / 8;
            },
            data: this.initData2(this.mapData),
          },
          {
            type: "effectScatter",
            coordinateSystem: "geo",
            zlevel: 2,
            rippleEffect: {
              brushType: "stroke",
            },
            label: {
              normal: {
                show: true,
                position: "right",
                formatter: "{b}",
              },
            },
            symbolSize: function (val) {
              return val[2] / 8;
            },
            itemStyle: {
              normal: {
                color: this.chartOption.endColor,
              },
            },
            data: this.initData2(this.mapData),
          }
        );
        var myChart = echarts.init(document.getElementById("mapChart"));
        myChart.setOption({
          backgroundColor: this.chartOption.backgroundColor,
          title: {
            left: 20,
            top: 10,
            textStyle: {
              fontSize: 16,
              fontFamily: "PingFangSC-Regular",
              fontWeight: "lighter",
              color: this.chartOption.titleColor,
            },
          },
          tooltip: {
            trigger: "item",
            formatter: (param) => {
              var data = param.data;
              return data.fromName + " - " + data.toName + " : " + data.value;
            },
          },
          legend: {
            orient: "vertical",
            top: "bottom",
            left: "right",
            selectedMode: "single",
          },
          geo: {
            map: "china",
            label: {
              emphasis: {
                show: false,
              },
            },
            roam: true,
            itemStyle: {
              normal: {
                areaColor: this.chartOption.areaColor,
                borderColor: this.chartOption.borderColor,
              },
              emphasis: {
                areaColor: this.chartOption.hoverAreaColor,
              },
            },
          },
          series: series,
        });
      });
    },
    initData1(data) {
      var reault = [];
      for (var i = 0; i < data.length; i++) {
        var el = data[i];
        var fromData = `${el.from_longitude},${el.from_latitude}`.split(",");
        var toData = `${el.to_longitude},${el.to_latitude}`.split(",");
        var val = [];
        val.push(fromData, toData);
        reault.push({
          fromName: el.from,
          toName: el.to,
          coords: val,
          value: el.num,
        });
      }
      return reault;
    },
    initData2(data) {
      var reault = [];
      for (var i = 0; i < data.length; i++) {
        var el = data[i];
        var val = `${el.to_longitude},${el.to_latitude},30`.split(",");
        reault.push({
          name: el.to,
          value: val,
        });
      }
      return reault;
    },
  },
  mounted() {
    this.mapChart();
  },
};
</script>
<style lang="scss" scoped>
.china {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 0 40px;
  box-sizing: border-box;
  .china-top {
    position: relative;
    height: 70%;
  }
}
.chart{
  position: absolute;
  left: -10%;
  top: -10%;
  width: 120%;
  height: 120%;
}
@keyframes loader-01 {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}

.map-bg {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: url('../../../assets/img/map_bg.b8b56475.png') no-repeat;
  background-size: 100% 100%;
  -webkit-animation: 10s loader-01  linear infinite;
  animation: 10s loader-01 linear infinite;
}
</style>