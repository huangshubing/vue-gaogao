<template>
  <div class="feed">
    <div class="feed_title w">
      <span class="feed_title_txt fl">供稿服务</span>
    </div>
    <ul class="feed_category w">
      <FeedItem v-for="(item, index) in data" :key="index" :data="item"></FeedItem>
    </ul>
  </div>
</template>

<script>
import FeedItem from "./Feed-item";
export default {
  components: {
    FeedItem
  },
  data() {
    return {
      data: [
        {
          img1: "https://ggapi.bqj.cn/image/new_index/feed_hs1.jpg",
          img2: "https://ggapi.bqj.cn/image/new_index/feed_cs1.jpg",
          type: "媒体稿件",
          txt: "MEDIA"
        },
        {
          img1: "https://ggapi.bqj.cn/image/new_index/feed_hs2.jpg",
          img2: "https://ggapi.bqj.cn/image/new_index/feed_cs2.jpg",
          type: "商业稿件",
          txt: "COMMERCIAL"
        },
        {
          img1: "https://ggapi.bqj.cn/image/new_index/feed_hs3.png",
          img2: "https://ggapi.bqj.cn/image/new_index/feed_cs3.png",
          type: "专业稿件",
          txt: "PROFESSIONAL"
        },
        {
          img1: "https://ggapi.bqj.cn/image/new_index/feed_hs4.jpg",
          img2: "https://ggapi.bqj.cn/image/new_index/feed_cs4.jpg",
          type: "图片图集",
          txt: "PICTURE"
        },
        {
          img1: "https://ggapi.bqj.cn/image/new_index/feed_hs5.jpg",
          img2: "https://ggapi.bqj.cn/image/new_index/feed_cs5.jpg",
          type: "短视频",
          txt: "VIDEO"
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
.feed {
  background-color: #fff;
  margin-top: 20px;
  padding-top: 40px;
  .feed_title {
    width: 100%;
    overflow: hidden;
    .feed_title_txt {
      text-align: left;
      font-size: 24px;
      display: inline-block;
      border-bottom: 3px solid #31a081;
      padding-bottom: 5px;
      margin: 0 8px 0 4px;
    }
  }
  .feed_category {
    overflow: hidden;
    .cli1 {
      width: 19.17%;
      background: #f1f3f4;
      display: inline-block;
      margin: 8px 4px 0;
      height: 200px;
      padding: 6px;
      border-radius: 5px;
      box-sizing: border-box;
      .category_box {
        position: relative;
        height: 94px;
        text-align: center;
        overflow: hidden;
        img {
          transition: all 1s ease 0s;
          position: absolute;
          top: 0;
          left: 0;
        }
      }
      .category_info {
        padding: 30px 15px 0;
        text-align: left;
        h3 {
          font-weight: normal;
          font-size: 18px;
          padding-bottom: 5px;
        }
        p {
          font-size: 14px;
          color: #ddd;
          font-weight: 600;
        }
      }
    }
  }
}
</style>
