<template>
  <div class="goods-item">
    <div class="goods-container">
      <div class="goods-container-img-frame">
        <img :src="goodsInfo.productThumb" alt="" class="thumb" />
      </div>
      <div class="title">{{ goodsInfo.productName }}</div>
      <div class="sales-tips">{{ goodsInfo.salesTips }}人付款</div>
      <div class="promotion">
        <div class="promotion-item coupon">
          {{ goodsInfo.couponDiscount }}元券
        </div>
        <div class="promotion-item profit">¥{{ goodsInfo.propProfit }}</div>
      </div>
      <div class="price">
        <div class="sale-price">¥{{ goodsInfo.productPrice }}</div>
        <div class="market-price">¥{{ goodsInfo.marketPrice }}</div>
      </div>
      <div class="store-">{{ goodsInfo.storeName }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    goodsInfo: {
      type: Object,
      default() {
        return {
          productThumb:
            "https://t7.baidu.com/it/u=1494424755,969945633&fm=193&f=GIF",
          productName:
            "realme 真我GT 大师探索版 120Hz三星AMOLED曲面屏 索尼IMX766传感器 骁龙870旅行箱·杏8GB+256GB 双模5G手机",
          salesTips: "1.5万",
          couponDiscount: 3,
          propProfit: 1.31,
          productPrice: 199,
          marketPrice: 240,
          storeName: "史努比千顺专卖店",
        };
      },
    },
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.goods-item {
  flex: 1 1 50%;
  box-sizing: border-box;
  padding: 8rpx;
  max-width: 50%;
  .goods-container {
    width: 100%;
    background-color: #fff;
    overflow: hidden;
    border-radius: 8rpx;
    &-img-frame {
      width: 100%;
      padding-bottom: 100%;
      position: relative;
      .thumb {
        display: block;
        position: absolute;
        width: 100%;
        height: 100%;
      }
    }
    .title {
      font-size: 24rpx;
      color: #333;
      overflow: hidden;
      text-overflow: ellipsis;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      line-height: 36rpx;
      margin: 10rpx;
    }
    .sales-tips {
      font-size: 20rpx;
      color: gray;
      line-height: 20rpx;
      margin: 10rpx;
    }
    .promotion {
      display: flex;
      padding: 0 10rpx;
      font-size: 20rpx;
      color: #f85aa0;
      &-item.coupon {
        border-radius: 4rpx;
        border: 2rpx solid #f85aa0;
        padding: 0 10rpx;
        margin-right: 10rpx;
        line-height: 30rpx;
      }
      &-item.profit {
        display: flex;
        align-items: center;
        padding: 0 10rpx;
        margin-right: 10rpx;
        line-height: 30rpx;
        height: 34rpx;
        border-radius: 4rpx;
        border: 2rpx solid #f85aa0;
        border-left: none;
        box-sizing: border-box;
        &::before {
          content: "预估返";
          display: block;
          height: 30rpx;
          background: linear-gradient(to right, #ffa8c9, #f85aa0);
          color: #fff;
          margin-right: 10rpx;
          margin-left: -10rpx;
          padding: 0 10rpx;
          border-top-left-radius: 4rpx;
          border-bottom-left-radius: 4rpx;
          border: 2rpx solid #f85aa0;
        }
      }
    }
  }
}
</style>