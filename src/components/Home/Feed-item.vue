<template>
  <li class="cli1 fl">
    <div class="category_box">
      <img :src="data.img1" class="img1" alt />
      <img :src="data.img2" class="img2" alt />
    </div>
    <div class="category_info">
      <h3>{{data.type}}</h3>
      <p>{{data.txt}}</p>
    </div>
  </li>
</template>

<script>
export default {
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
    .img1 {
      // transition: all 1s ease 0s;
      // position: absolute;
      // top: 0;
      // left: 0;
      width: 100%;
    }
    .img2 {
      display: none;
    }
  }
  .category_info {
    padding: 30px 15px 0;
    text-align: left;
    height: 100%;
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
.cli1:hover {
  .category_box {
    .img1 {
      display: none;
    }
    .img2 {
      display: block;
      position: relative;
      // width: 105%;
      // height: 105%;
      // left: -5%;
      // top: -5%;
      // transition: all 6s;
      animation: big 0.6s ease-in-out 1 forwards;
      @keyframes big {
        from {
          width: 100%;
          left: 0%;
          top: 0%;
        }
        to {
          width: 110%;
          left: -5%;
          top: -5%;
        }
      }
    }
  }
  .category_info {
    background-color: #434343;
    color: #fff;
    box-shadow: 2px 2px 8px 2px rgba(0, 0, 0, 0.2);
    transition: all 0.6s;
  }
}
</style>
