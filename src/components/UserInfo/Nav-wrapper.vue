<template>
  <div class="nav_wrapper">
    <p>我要卖稿</p>
    <ul>
      <!-- navData.current*3 + 1 -->
      <li @click="get(1)" :class="result == 1 ? 'active' : '' ">
        <i :class="navData.icon_class1"></i>
        <span>{{navData.icon_txt1}}</span>
      </li>
      <li @click="get(2)" :class="result == 2 ? 'active' : '' ">
        <i :class="navData.icon_class2"></i>
        <span>{{navData.icon_txt2}}</span>
      </li>
      <li @click="get(3)
      " :class="result == 3 ? 'active' : '' ">
        <i :class="navData.icon_class3"></i>
        <span>{{navData.icon_txt3}}</span>
      </li>
    </ul>
    <div class="line"></div>
  </div>
</template>  

<script>
export default {
  name: "UserInfoNavWrapper",
  data() {
    return {
      result: 1
    };
  },
  props: {
    navData: {
      type: Object,
      default: {}
    }
  },
  methods: {
    get: function(params) {
      this.result = params;
      this.$router.push(`/userInfo/${params}`);
      console.log(this.result);
    }
  },
  mounted() {
    this.result = this.$route.params.id;
  }
};
</script>

<style lang="less" scoped>
.nav_wrapper {
  .line {
    margin-top: 15px;
    margin-bottom: 30px;
    width: 80%;
    height: 1px;
    background-color: #ccc;
  }
  p {
    font-size: 16px;
    color: #000;
  }
  ul {
    margin-top: 20px;
    li {
      color: #666;
      box-sizing: border-box;
      font-size: 14px;
      cursor: pointer;
      margin-bottom: 20px;
      height: 30px;
      line-height: 20px;
      i {
        margin: 2px 10px 0 0;
      }
      span {
        font-size: 14px;
      }
      &.active {
        color: #31a081;
        span {
          padding-bottom: 2px;
          border-bottom: 2px solid #31a081;
        }
      }
    }
    li:hover {
      color: #31a081;
      span {
        padding-bottom: 2px;
        border-bottom: 2px solid #31a081;
      }
    }
  }
}
</style>