<template>
  <div class="price">
    <div id="price"></div>
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
        xAxis: {
          type: 'category',
          boundaryGap: false,
          data: ['07:23', '08:23', '09:23', '10:23', '11:23', '12:23', '13:23'].map((item) => ({
            value: item,
            textStyle: { color: "#fff" },
          })),
          nameTextStyle: {
            color: "#fff",
          },
          axisLine: {
            show: false,
          },
          axisTick: {
            show: false,
          },
        },
        yAxis: {
          type: 'value',
          splitLine: {
            lineStyle: {
              type: "dashed",
              color: "#fff",
            },
          },
          axisLabel: {
            show: true,
            textStyle: {
              color: "#fff",
            },
          },
        },
        series: [
          {
            data: [10, 49, 22, 32, 32, 32, 32],
            type: 'line',
            areaStyle: {
              color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                { offset: 0, color: "#e6911f" },
                { offset: 0.4, color: "#e6911f" },
                { offset: 1, color: "#83bff600" },
              ]),
            },
            lineStyle: {
              color: '#e6911f'
            },
            itemStyle: {
              color: '#e6911f'
            }
          }
        ]
      };
      var myChart = echarts.init(document.getElementById("price"));
      myChart.setOption(option);
    },
  },
};
</script>

<style lang="scss" scoped>
.price {
  width: 300px;
  height: 200px;
  #price {
    width: 300px;
    height: 200px;
  }
}
</style>