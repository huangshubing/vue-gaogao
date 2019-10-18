<template>
  <div class="rare w">
    <div class="rare_title">
      <span class="rare_title_txt fl">百里挑一</span>
    </div>
    <p>稿稿御用高端创作者社群，汇集平台最顶尖的创作者，俱乐部成员享受专属vip特权，高薪+特权 C位出道</p>
    <ul class="rare_category w">
      <div class="swiper-container">
        <div class="swiper-wrapper">
          <div class="swiper-slide swiper-slide1">
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_01.png" alt />
              </div>
              <div class="category_info">
                <h3>媒体稿件</h3>
                <div class="mess">
                  <span>钻石写手</span>
                </div>
                <p>累计写稿305篇</p>
                <p>时事热点/情感/生活窍门</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_02.png" alt />
              </div>
              <div class="category_info">
                <h3>商业稿件</h3>
                <div class="mess">
                  <span>钻石写手</span>
                </div>
                <p>累计写稿305篇</p>
                <p>时事热点/情感/生活窍门</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_03.png" alt />
              </div>
              <div class="category_info">
                <h3>专业稿件</h3>
                <div class="mess">
                  <span>钻石写手</span>
                </div>
                <p>累计写稿305篇</p>
                <p>时事热点/情感/生活窍门</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_04.png" alt />
              </div>
              <div class="category_info">
                <h3>图片图集</h3>
                <div class="mess">
                  <span>钻石写手</span>
                </div>
                <p>累计写稿305篇</p>
                <p>时事热点/情感/生活窍门</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_05.png" alt />
              </div>
              <div class="category_info">
                <h3>短视频</h3>
                <div class="mess">
                  <span>钻石写手</span>
                </div>
                <p>累计写稿305篇</p>
                <p>时事热点/情感/生活窍门</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_05.png" alt />
              </div>
              <div class="category_info">
                <h3>短视频</h3>
                <div class="mess">
                  <span>钻石写手</span>
                </div>
                <p>累计写稿305篇</p>
                <p>时事热点/情感/生活窍门</p>
              </div>
            </li>
          </div>
          <div class="swiper-slide swiper-slide2">
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_01.png" alt />
              </div>
              <div class="category_info">
                <h3>媒体稿件</h3>
                <p>MEDIA</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_02.png" alt />
              </div>
              <div class="category_info">
                <h3>商业稿件</h3>
                <p>COMMERCIAL</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_03.png" alt />
              </div>
              <div class="category_info">
                <h3>专业稿件</h3>
                <p>PROFESSIONAL</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_04.png" alt />
              </div>
              <div class="category_info">
                <h3>图片图集</h3>
                <p>PICTURE</p>
              </div>
            </li>
            <li class="cli1 fl">
              <div class="category_box">
                <img src="../../assets/img/feed_blank_05.png" alt />
              </div>
              <div class="category_info">
                <h3>短视频</h3>
                <p>VIDEO</p>
              </div>
            </li>
          </div>
        </div>
      </div>
    </ul>
  </div>
</template>

<script>
import Swiper from "swiper";
import "swiper/css/swiper.min.css";
export default {
  props: {
    msg: String
  },
  mounted() {
    var mySwiper = new Swiper(".swiper-container", {
      autoplay: false,
      loop: true
    });
  }
};
</script>

<style scoped lang="less">
.rare {
  background-color: #fff;
  margin-top: 20px;
  padding-top: 40px;
  p {
    margin-top: 15px;
    margin-bottom: 30px;
    text-align: left;
    padding-left: 15px;
    font-size: 16px;
    color: #666;
  }
  .rare_title {
    width: 98%;
    overflow: hidden;
    border-bottom: 1px solid #ddd;
    margin-top: 40px;
    margin: 0 15px;
    .rare_title_txt {
      text-align: left;
      font-size: 24px;
      display: inline-block;
      border-bottom: 3px solid #31a081;
      padding-bottom: 5px;
      // margin: 0 8px 0 4px;
    }
  }
  .rare_category {
    width: 80%;
    overflow: hidden;
    .swiper-container {
      // background: rgb(100, 161, 226);
      .swiper-slide1 {
        background-color: #333;
      }
      .swiper-slide2 {
        background-color: #64a1e2;
      }
    }
    .cli1 {
      width: 10%;
      background: #f1f3f4;
      display: inline-block;
      margin: 3% 3.3% 0;
      // height: 200px;
      // padding: 6px;
      // border-radius: 5px;
      // box-sizing: border-box;
      .category_box {
        position: relative;
        height: 95px;
        text-align: center;
        overflow: hidden;
        img {
          // transition: all 1s ease 0s;
          // position: absolute;
          // top: 0;
          // left: 0;
          width: 90px;
          height: 90px;
          border-radius: 50%;
        }
      }
      .category_info {
        font-size: 18px;
        color: #000;
        padding: 30px 0 0;
        text-align: center;
        h3 {
          font-weight: normal;
          font-size: 18px;
          padding-bottom: 5px;
        }
        p {
          font-size: 14px;
          color: #ddd;
          font-weight: 600;
          padding: 0;
          margin: 0;
          display: none;
        }
        p:last-child {
          font-size: 12px;
        }
        .mess {
          background: #6d9ede;
          display: inline-block;
          border-radius: 10px;
          padding: 3px 6px;
          // margin: 5px 0 10px;
          display: none;
          font-size: 12px;
        }
      }
    }
    .cli1:hover {
      width: 16.6%;
      // height: 280px;
      margin: 0;
      .category_box {
        padding-top: 20px;
        img {
          width: 95px;
          height: 95px;
        }
      }
      .category_info {
        p {
          text-align: center;
          line-height: 21px;
          display: block;
        }
        .mess {
          width: 35%;
          margin: 5px auto;
          display: block;
        }
      }
    }
  }
}
</style>
