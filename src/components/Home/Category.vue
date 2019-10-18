<template>
  <ul class="category w">
    <CategoryItem v-for="(item, index) in data" :key="index" :data="item"></CategoryItem>
  </ul>
</template>

<script>
import CategoryItem from "./Category-item";
export default {
  components: {
    CategoryItem
  },
  data() {
    return {
      data: [
        {
          type: "商稿",
          img: "http://ggoss.bqj.cn/20190524/image/3/1558685625935282.png"
        },
        {
          type: "自媒体",
          img: "http://ggoss.bqj.cn/20190524/image/3/1558685647292222.png"
        },
        {
          type: "短视频",
          img: "http://ggoss.bqj.cn/20190524/image/3/1558685663518266.png"
        },
        {
          type: "专业稿件",
          img: "http://ggoss.bqj.cn/20190524/image/3/1558685655442669.png"
        },
        {
          type: "素材征集",
          img: "http://ggoss.bqj.cn/20190524/image/3/1558685670973101.png"
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

<style scoped lang="less">
.category {
  padding-top: 15px;
  overflow: hidden;
}
</style>
