<template>
  <div class="container">
    <div class="nav_content w">
      <div class="left_nav fl">
        <div class="my_home">
          <span>我的主页</span>
          <div class="line"></div>
        </div>
        <UserInfoNavWrapper v-for="(item, index) in navData" :key="index" :navData="item" />
      </div>
      <div class="nav_main">
        <UserInfoNavItem />
      </div>
    </div>
  </div>
</template>  

<script>
import NavBar from "@/components/UserInfo/Nav-bar.vue";
import UserInfoNavWrapper from "@/components/UserInfo/Nav-wrapper.vue";
import UserInfoNavItem from "@/components/UserInfo/Nav-item.vue";
export default {
  components: {
    NavBar,
    UserInfoNavWrapper,
    UserInfoNavItem
  },
  data() {
    return {
      navData: [
        {
          current: 0,
          wrapper_title: "我要卖稿",
          icon_txt1: "稿件箱",
          icon_class1: "iconfont iconxiangzi",
          icon_txt2: "自助投稿",
          icon_class2: "iconfont iconzhifeiji",
          icon_txt3: "委托投稿",
          icon_class3: "iconfont iconzhifeiji"
        },
        {
          current: 1,
          wrapper_title: "我的账户",
          icon_txt1: "账户资金",
          icon_class1: "iconfont iconqian",
          icon_txt2: "账户设置",
          icon_class2: "iconfont iconzhanghushezhi",
          icon_txt3: "消息中心",
          icon_class3: "iconfont iconuser-reply"
        }
      ]
    };
  },
  props: {
    msg: String,
    default: "no data"
  }
};
</script>

<style lang="less" scoped>
.container {
  background-color: #f7f7f7;
  padding-top: 67px;
  .nav_content {
    margin-top: 15px;
    .left_nav {
      width: 130px;
      text-align: left;
      .my_home {
        padding-right: 15px;
        span {
          color: #31a081;
          padding-bottom: 2px;
          border-bottom: 2px solid #31a081;
        }
        .line {
          margin-top: 15px;
          margin-bottom: 30px;
          width: 80%;
          height: 1px;
          background-color: #ccc;
        }
      }
    }
  }
}
</style>