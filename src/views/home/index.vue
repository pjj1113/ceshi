<template>
  <div class="home">
    <h2></h2>
    <div class="tabbar">
      <div class="box" v-for="(item, index) in labelList" :key="index">
        <ul>
          <li v-for="(list, index) in item.list" :key="index">
            <a :href="list.route" :target="list.blank ? '_blank' : ''">{{ list.name }}</a>
          </li>
        </ul>
        <div class="content">
          <i></i>
          <span>{{ item.title }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      labelList: [
        { title:'数字乡村', icon: '', show: false, list:[
          { name: '数字乡村一张图', route: '/platform' },
          { name: '农村宅基地管理', route: '#' },
          { name: '智慧农业', route: '#' },
          { name: '特色产业', route: '#' },
          { name: '食品溯源', route: '#' },
          { name: '蓝天卫视', route: '#' },
          { name: '三资管理', route: '#' }
        ]},
        {  title:'数字治理', icon: '', show: false, list:[
          { name: '智慧建党', route: 'https://www.aidjyun.com/portal/login',blank: true },
          { name: '阳光村务', route: '/sunVillage' },
          { name: '智慧城管', route: '#' },
          { name: '雪亮工程', route: '#' },
          { name: '智慧交通', route: '#' },
          { name: '微单元治理', route: '#' },
        ] },
        {  title:'民生服务', icon: '', show: false, list:[
          { name: '政务服务', route: '#' },
          { name: '智慧医疗', route: '#' },
          { name: '智慧教育', route: '#' },
          { name: '智慧社区', route: '#' },
          { name: '智慧养老', route: 'http://39.99.202.55:6655/Home/index', blank: true },
        ] }
      ]
    }
  },
  mounted() {

  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  background: url('../../assets/img/xx_bg.2ac84150.jpg') no-repeat;
  h2 {
    width: 60%;
    height: 50px;
    background: url('../../assets/img/xx_title.160bedd4.png') no-repeat;
    background-size: 100% 100%;
    margin-bottom: 20px;
  }
  .tabbar {
    display: flex;
    justify-content: center;
    width: 100%;
    padding: 30;
    // background: rgba(104,218,208,.5);
    .box {
      position: relative;
      width: 250px;
      height: 250px;
      margin-right: 40px;
      border-radius: 8px;
      overflow: hidden;
      .content {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
        background: rgba(104,218,208,.5);
        i {
          display: inline-block;
          width: 130px;
          height: 93px;
          transform: scale(0.8);
          background: url(/static/img/nav_icon.b48a76a3.b48a76a3.png) 0px -93px no-repeat;
          background-size: 100%;
          margin: 0.416667rem 0px 0.197917rem;
        }
        span {
          color: #fff;
          font-size: 18px;
        }
      }
      ul {
        position: absolute;
        left: 0;
        top: -300px;
        width: 100%;
        height: 100%;
        z-index: 100;
        box-sizing: border-box;
        padding: 20px;
        background: rgba($color: #fff, $alpha: .5);
        transition: top 1s;
        li {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          font-size: 15px;
          margin-bottom: 10px;
        }
      }
      &:hover ul{
        top: 0;
      }
    }
  }
}
</style>