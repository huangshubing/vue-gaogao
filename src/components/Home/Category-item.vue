<template>
  <li class="cli1 fl">
    <div class="category_box">
      <img :src="data.img" alt />
    </div>
    <div class="category_info">{{data.type}}</div>
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
.category {
  padding-top: 15px;
  overflow: hidden;
  .cli1 {
    width: 19.17%;
    background: #fff;
    display: inline-block;
    margin: 8px 4px 0;
    height: 160px;
    padding: 6px;
    border-radius: 5px;
    box-sizing: border-box;
    cursor: pointer;

    .category_box {
      position: relative;
      height: 94px;
      text-align: center;
      img {
        width: 56px;
        height: 56px;
        border-radius: 5px;
        margin-top: 24px;
      }
    }
    .category_info {
      width: 100%;
      padding: 12px 10px 0;
      position: relative;
      box-sizing: border-box;
    }
  }
}
</style>
