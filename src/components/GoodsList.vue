<template>
  <div class="goods-list">
    <GoodsItem></GoodsItem>
    <GoodsItem></GoodsItem>
    <GoodsItem></GoodsItem>
    <GoodsItem></GoodsItem>
    <GoodsItem></GoodsItem>
    <GoodsItem></GoodsItem>
    <GoodsItem></GoodsItem>
  </div>
</template>

<script>
import GoodsItem from "./GoodsItem.vue";
export default {
  components: {
    GoodsItem,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.goods-list {
  display: flex;
  flex-wrap: wrap;
  box-sizing: border-box;
  padding: 10rpx 0;
}
</style>