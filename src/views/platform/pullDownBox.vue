<template>
  <div class="pull-down-box">
    <div class="pull-list" v-for="(item, i) in dataList" :key="i">
      <ul v-show="item.flag">
        <li v-for="(item, index) in item.list" :key="index"> <el-checkbox v-model="item.isSelect">{{ item.name }}</el-checkbox></li>
      </ul>
      <a @click="showSelect(i)">基础数据</a>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    // list: {
    //   type: Array,
    //   default:()=>[]
    // }
  },
  data() {
    return {
      flag: false,
      dataList: [
        {
          flag: false,
          list: [
            { name: '土地规划', isSelect: false },
            { name: '基本农田', isSelect: false },
            { name: '高标准农田', isSelect: false },
            { name: '农村宅基地', isSelect: false },
            { name: '农村集体建设用地', isSelect: false },
            { name: '设施农用地', isSelect: false },
            { name: '三调', isSelect: false },
            { name: '两区划定', isSelect: false },
            { name: '土地承包经营权', isSelect: false },
          ],
        },
        {
          flag: false,
          list: [
          { name: '章墩产业', isSelect: false },
            { name: '经营主体', isSelect: false },
            { name: '香菇', isSelect: false },
            { name: '再生稻', isSelect: false },
            { name: '稻 虾', isSelect: false },
          ],
        },
        {
          flag: false,
          list: [
            { name: '垃圾屋', isSelect: false },
            { name: '垃圾站点池', isSelect: false },
            { name: '污水井盖', isSelect: false },
          ],
        },
        {
          flag: false,
          list: [
            { name: '村委会', isSelect: false },
            { name: '乡村卫生站', isSelect: false },
            { name: '慢病管理', isSelect: false },
            { name: '避灾场所', isSelect: false },
            { name: '益农信息社', isSelect: false },
            { name: '新村部', isSelect: false },
          ],
        },
        {
          flag: false,
          list: [
          { name: '党员户', isSelect: false },
          { name: '党员户党员户', isSelect: false },
          { name: '贫困户', isSelect: false },
          { name: '视频监控', isSelect: false },
          { name: '环境监测', isSelect: false },
        ]
        }
      ]
    }
  },
  methods: {
    showSelect(i) {
      this.dataList[i].flag = !this.dataList[i].flag
    }
  }
}
</script>

<style lang="scss" scoped>
.pull-down-box {
  position: absolute;
  bottom: 30px;
  z-index: 500;
  width: 100%;
  display: flex;
  justify-content: space-around;
  ul {
    position: absolute;
    bottom: 40px;
    padding: 10px;
    width: 150px;
    box-sizing: border-box;
    background: rgba(33,63,76,.8);
    border: 1px solid #199992;
  }
  a {
    display: inline-block;
    height: 35px;
    width: 150px;
    text-align: center;
    line-height: 35px;
    color: #fff;
    font-size: 15px;
    background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAKwAAAA4CAYAAABgxhONAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyNpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDYuMC1jMDAyIDc5LjE2NDQ4OCwgMjAyMC8wNy8xMC0yMjowNjo1MyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wTU09Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9tbS8iIHhtbG5zOnN0UmVmPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvc1R5cGUvUmVzb3VyY2VSZWYjIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6ODJEMDU4MzRCOUY3MTFFQjgzOEZCNTYzNEI5QkM5MEQiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6ODJEMDU4MzNCOUY3MTFFQjgzOEZCNTYzNEI5QkM5MEQiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIDIyLjAgKFdpbmRvd3MpIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6RUUyNjM0OThCOUVGMTFFQjg0QzVDRjU1RkM2QTgwMzUiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6RUUyNjM0OTlCOUVGMTFFQjg0QzVDRjU1RkM2QTgwMzUiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz7RXmwLAAAK50lEQVR42uxdO5Ik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) no-repeat;
    background-size: 100% 100%;
  }
}
.pull-list {
  
}
/deep/.el-checkbox__label {
  color: #fff;
}
/deep/.el-checkbox__input.is-checked+.el-checkbox__label {
  color: #199992;
}
/deep/.el-checkbox__input.is-checked .el-checkbox__inner, .el-checkbox__input.is-indeterminate .el-checkbox__inner {
  background-color: #199992;
  border-color: #199992;
}
</style>