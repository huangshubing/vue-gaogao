<template>
  <li class="cli1 fl">
    <a href="#">
      <div class="content_box">
        <slot :data="data.img"></slot>
      </div>
      <div class="content_info">
        <div class="sp1">{{data.price}}</div>
        <div class="info_txt">{{data.title}}</div>
        <div class="info_type">{{data.type}}</div>
        <div class="info_time">
          <p>
            <i class="iconfont icon00FE"></i>
            <span class="timecount">{{data.time}}天</span>
            <span class="sp2">欲购稿件量: {{data.number}}篇</span>
          </p>
        </div>
        <div class="info_bottom">
          <div class="userP fr">
            <div class="cir1 fl">
              <Vicon :data="data.users"></Vicon>
            </div>
            <i class="cirline"></i>
            <span class="cir2 fr">
              <i class="iconfont iconzhifeiji"></i>
            </span>
          </div>
        </div>
      </div>
    </a>
  </li>
</template>

<script>
import Vicon from "./Collect-item-icon";
export default {
  components: {
    Vicon
  },
  props: {
    data: {
      type: Object,
      default: {}
    }
  },
  mounted() {
    // console.log(this.data);
  }
};
</script>

<style scoped lang="less">
.collect {
  color: #000;
  .collect_title {
    width: 100%;
    overflow: hidden;
    .collect_title_txt {
      text-align: left;
      font-size: 24px;
      display: inline-block;
      border-bottom: 3px solid #31a081;
      padding-bottom: 5px;
      margin: 0 8px 0 4px;
    }
  }
  .collect_content {
    padding: 12px 0 10px;
    .cli1:hover {
      box-shadow: 0px 0px 10px 0px #333;
      width: 33.1%;
      margin: 8px 0 0;
    }
    .cli1 {
      width: 32.26%;
      background: #fff;
      // border-radius: 5px;
      margin: 8px 4px 0;
      height: 398px;
      padding: 6px;
      box-sizing: border-box;
      transition: all 0.25s linear;
      a {
        color: #000;
        .content_box {
          width: 100%;
          img {
            width: 100%;
            border-radius: 5px;
          }
        }
        .content_info {
          width: 100%;
          padding: 12px 10px 0;
          position: relative;
          box-sizing: border-box;
          .sp1 {
            color: #31a081;
            font-size: 24px;
            padding-bottom: 5px;
          }
          .info_txt {
            font-size: 18px;
            line-height: 24px;
            height: 50px;
            font-weight: 300;
            padding: 0 25px;
          }
          .info_type {
            padding: 3px 10px 4px;
            border-radius: 50px;
            color: #888;
            font-size: 12px;
            display: inline-block;
            border: 1px solid #cdcdcd;
          }
          .info_time {
            padding: 8px 0;
            margin-top: 15px;
            border-bottom: 1px dashed #eeeeee;
            border-top: 1px dashed #eeeeee;
            color: #666;
            font-weight: 300;
            font-size: 14px;
            text-align: left;
            i {
              font-size: 22px;
              color: #888888;
              vertical-align: middle;
            }
            .sp2 {
              float: right;
              vertical-align: middle;
              color: #888888;
              font-weight: 300;
              font-size: 13px;
            }
          }
          .info_bottom {
            display: inline-block;
            width: 100%;
            .userP {
              height: 28px;
              width: 140px;
              text-align: right;
              padding: 20px 0;
              position: relative;
              .cir1 {
                display: inline-block;
                width: 75px;
                position: relative;
                margin-bottom: 20px;
                .circle {
                  bottom: -28px;
                  position: absolute;
                  width: 35px;
                  height: 35px;
                  border-radius: 50%;
                  .tooltip1 {
                    display: none;
                  }
                  img {
                    width: 100%;
                    border-radius: 50%;
                  }
                  &.circle01 {
                    right: 0;
                    z-index: 10;
                  }
                  &.circle02 {
                    right: 18px;
                    z-index: 9;
                  }
                }
                .circle:hover {
                  width: 38px;
                  height: 38px;
                  .tooltip1 {
                    white-space: nowrap;
                    display: block;
                    color: #fff;
                    background: #1f2d3d;
                    border-radius: 5px;
                    padding: 10px 10px;
                    position: absolute;
                    font-size: 12px;
                    top: -52px;
                    text-align: center;
                    .jiao {
                      width: 0;
                      height: 0;
                      border-top: 7px solid #000;
                      border-left: 7px solid #fff;
                      border-right: 7px solid #fff;
                      position: relative;
                      top: 17px;
                      left: 48%;
                    }
                  }
                }
              }
              .cirline {
                padding-right: 1px;
                display: inline-block;
                height: 35px;
                background: #eee;
                margin-right: 15px;
                margin-top: -8px;
              }
              .cir2 {
                position: relative;
                background: #eee;
                width: 35px;
                height: 35px;
                border-radius: 50%;
                line-height: 42px;
                text-align: center;
                display: inline-block;
                vertical-align: top;
                top: -6px;
                margin-bottom: 20px;
                i {
                  font-family: "iconfont" !important;
                  color: rgb(49, 160, 129);
                  font-size: 24px;
                  line-height: 28px;
                  font-style: normal;
                }
              }
              .cir2:hover {
                background-color: green;
                i {
                  color: #fff;
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>
