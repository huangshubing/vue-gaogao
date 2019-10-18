<template>
  <div class="collect w">
    <div class="collect_title">
      <span class="collect_title_txt fl">征稿令</span>
    </div>
    <ul class="collect_content">
      <CollectItem v-for="(item,index) in data" :key="index" :data="item">
        <template slot-scope="data">
          <img :src="data.data" />
          <!-- <div class="tmpl">{{data}}

          </div>-->
        </template>

        <!-- <img slot="img" :src="item.img" alt /> -->
      </CollectItem>
    </ul>
  </div>
</template>

<script>
import CollectItem from "./Collect-item";
export default {
  components: {
    CollectItem
  },
  data() {
    return {
      data: [
        {
          price: "￥150~￥250",
          title: "长期大量征——原创  国内自驾游/落地游攻略/游记",
          type: "旅游",
          time: "6",
          number: "1",
          img:
            "http://ggoss.bqj.cn/20191017/image/3/1571303840909300.jpg?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥150~￥200",
          title: "“推荐式影评/影人系列” 征稿",
          type: "电影音乐",
          time: "5",
          number: "2",
          img:
            "http://ggoss.bqj.cn/20190925/image/3/1569382228905276.png?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥300~￥350",
          title: "野外美食搞笑创意脚本",
          type: "视频创意 / 视频脚本",
          time: "1",
          number: "1",
          img: "https://ggapi.bqj.cn/image/fillyList.png",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥200~￥250",
          title: "干货 育儿 婚姻 情感干货",
          type: "情感 / 教育 / 母婴育儿",
          time: "6",
          number: "2",
          img:
            "http://ggoss.bqj.cn/20191017/image/3/1571294355901569.jpg?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥400~￥450",
          title: "【定制稿】为销帮帮CRM“客户管理”版块撰写产品文案",
          type: "商品介绍",
          time: "5",
          number: "1",
          img: "https://ggapi.bqj.cn/image/fillyList.png",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥150~￥200",
          title: "美妆个护搞笑视频脚本",
          type: "视频创意 / 视频脚本",
          time: "4",
          number: "1",
          img:
            "http://ggoss.bqj.cn/20191015/image/3/1571132684882830.jpg?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥500~￥700",
          title: "城乡规划、建筑家装、市政园林设计征稿",
          type: "教育 / 时事热点 / 艺术文化",
          time: "4",
          number: "3",
          img:
            "http://ggoss.bqj.cn/20190902/image/3/1567407116353570.png?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥200~￥250",
          title: "正心正举哲学主题征稿（20个主题）",
          type: "文学",
          time: "3",
          number: "1",
          img:
            "http://ggoss.bqj.cn/20190929/image/3/1569726308583397.jpg?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
        },
        {
          price: "￥300~￥500",
          title: "“科研趣事分享”主题征稿",
          type: "教育",
          time: "3",
          number: "1",
          img:
            "http://ggoss.bqj.cn/20190807/image/3/1565158598994343.jpg?x-oss-process=image/resize,w_300",
          users: [
            {
              icon:
                "http://ggoss.bqj.cn/20191009/image/3/1570626086686905.jpg?x-oss-process=image/resize,w_46",
              content: "小竹 * / 自驾游功..."
            },
            {
              icon:
                "http://thirdwx.qlogo.cn/mmopen/kMaz9nc8bgKL0Nkb5KwxibCVko3usVQ1FUzxzERz5uO3VcmuVBrw4Y2V8e2UmicELZxOhqJpZ1zQj952OM0D7KMntjvc5K92WY/132",
              content: "会飞 * / 印度极品..."
            }
          ]
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
  // .collect_content {
  //   padding: 12px 0 10px;
  //   .cli1:hover {
  //     box-shadow: 0px 0px 10px 0px #333;
  //     width: 33%;
  //   }
  //   .cli1 {
  //     width: 32.26%;
  //     background: #fff;
  //     // border-radius: 5px;
  //     margin: 8px 4px 0;
  //     height: 398px;
  //     padding: 6px;
  //     box-sizing: border-box;
  //     transition: all 0.25s linear;
  //     a {
  //       color: #000;
  //       .content_box {
  //         img {
  //           border-radius: 5px;
  //         }
  //       }
  //       .content_info {
  //         width: 100%;
  //         padding: 12px 10px 0;
  //         position: relative;
  //         box-sizing: border-box;
  //         .sp1 {
  //           color: #31a081;
  //           font-size: 24px;
  //           padding-bottom: 5px;
  //         }
  //         .info_txt {
  //           font-size: 18px;
  //           line-height: 24px;
  //           height: 50px;
  //           font-weight: 300;
  //           padding: 0 25px;
  //         }
  //         .info_type {
  //           padding: 3px 10px 4px;
  //           border-radius: 50px;
  //           color: #888;
  //           font-size: 12px;
  //           display: inline-block;
  //           border: 1px solid #cdcdcd;
  //         }
  //         .info_time {
  //           padding: 8px 0;
  //           margin-top: 15px;
  //           border-bottom: 1px dashed #eeeeee;
  //           border-top: 1px dashed #eeeeee;
  //           color: #666;
  //           font-weight: 300;
  //           font-size: 14px;
  //           text-align: left;
  //           i {
  //             font-size: 22px;
  //             color: #888888;
  //             vertical-align: middle;
  //           }
  //           .sp2 {
  //             float: right;
  //             vertical-align: middle;
  //             color: #888888;
  //             font-weight: 300;
  //             font-size: 13px;
  //           }
  //         }
  //         .info_bottom {
  //           display: inline-block;
  //           width: 100%;
  //           .userP {
  //             height: 28px;
  //             width: 140px;
  //             text-align: right;
  //             padding: 20px 0;
  //             position: relative;
  //             .cir1 {
  //               display: inline-block;
  //               width: 75px;
  //               position: relative;
  //               margin-bottom: 20px;
  //               .circle {
  //                 bottom: -28px;
  //                 position: absolute;
  //                 width: 35px;
  //                 height: 35px;
  //                 border-radius: 50%;
  //                 img {
  //                   width: 100%;
  //                   border-radius: 50%;
  //                 }
  //                 &.circle01 {
  //                   right: 0;
  //                   z-index: 10;
  //                 }
  //                 &.circle02 {
  //                   right: 18px;
  //                   z-index: 9;
  //                 }
  //                 .tooltip1 {
  //                   display: none;
  //                 }
  //                 &.tooltip {
  //                   .tooltip1 {
  //                     white-space: nowrap;
  //                     color: #fff;
  //                     background: #1f2d3d;
  //                     border-radius: 5px;
  //                     padding: 10px 10px;
  //                     position: absolute;
  //                     font-size: 12px;
  //                     top: -52px;
  //                     text-align: center;
  //                     display: block;
  //                     .jiao {
  //                       width: 0;
  //                       height: 0;
  //                       border-top: 7px solid #000;
  //                       border-left: 7px solid #fff;
  //                       border-right: 7px solid #fff;
  //                       position: relative;
  //                       top: 17px;
  //                       left: 48%;
  //                     }
  //                   }
  //                 }
  //               }
  //             }
  //             .cirline {
  //               padding-right: 1px;
  //               display: inline-block;
  //               height: 35px;
  //               background: #eee;
  //               margin-right: 15px;
  //               margin-top: -8px;
  //             }
  //             .cir2 {
  //               position: relative;
  //               background: #eee;
  //               width: 35px;
  //               height: 35px;
  //               border-radius: 50%;
  //               line-height: 42px;
  //               text-align: center;
  //               display: inline-block;
  //               vertical-align: top;
  //               top: -6px;
  //               margin-bottom: 20px;
  //               i {
  //                 font-family: "iconfont" !important;
  //                 color: rgb(49, 160, 129);
  //                 font-size: 24px;
  //                 line-height: 28px;
  //                 font-style: normal;
  //               }
  //             }
  //           }
  //         }
  //       }
  //     }
  //   }
  // }
}
</style>
