<script setup lang="ts">
// import { uni-icons } from '@dcloudio/uni-ui'

// const { title, changeTitle } = useTitle();
// function goTest() {
//   forward('test', {
//     a: 1
//   });
// }
const bannerList = computed(() => {
  return [
    '/static/images/banner1.jpg',
    '/static/images/banner2.jpg',
    '/static/images/banner3.jpg'
  ];
});
</script>

<template>
  <view class="home">
    <view class="banner">
      <swiper class="swiper" circular indicator-dots autoplay>
        <swiper-item
          v-for="(item, index) in bannerList"
          :key="index"
          class="swiper-item"
        >
          <image class="swiper-image" :src="item" mode="aspectFill"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="notice">
      <view class="left">
        <uni-icons type="sound-filled" size="20"></uni-icons>
        <text class="text">公告</text>
      </view>
      <view class="center">
        <swiper
          class="swiper-v"
          vertical
          autoplay
          interval="1500"
          duration="300"
          circular
        >
          <swiper-item v-for="item in 4" :key="item" class="swiper-v-item">
            文字内容发给睡觉的的接电话好动画回大ddfhdhdjkhfjdkhfkjdhfkjdhfkjdhfjhdk幅度的
            的的的的 家回家换手机h</swiper-item
          >
        </swiper>
      </view>
      <view class="right">
        <uni-icons type="right" size="16" color="#333"></uni-icons>
      </view>
    </view>
  </view>
</template>

<style scoped lang="scss">
.home {
  box-sizing: border-box;
  .banner {
    box-sizing: border-box;
    .swiper {
      box-sizing: border-box;
      padding: 30rpx 0;
      width: 100vw;
      height: 340rpx; /* 根据需要调整高度 */
      .swiper-item {
        display: flex;
        justify-content: center;
        align-items: center;
        box-sizing: border-box;
        .swiper-image {
          padding: 0 30rpx;
          width: 100%; /* 根据需要调整宽度，或者保持auto以使用图片的原始宽度 */
          height: 100%; /* 保持图片的原始比例 */
        }
      }
    }
  }
  .notice {
    display: flex;
    margin: 0 auto;
    border-radius: 80rpx;
    width: 100%;
    height: 80rpx;
    background: #f9f9f9;
    line-height: 80rpx;
    .left {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 140rpx;
      .text {
        font-weight: 600;
        font-size: 28rpx;
        color: $uni-color-success;
      }
    }
    .center {
      flex: 1;
      // width: 100%;
      .swiper-v {
        height: 100%;
        .swiper-v-item {
          overflow: hidden;
          height: 100%;
          text-overflow: ellipsis;
          font-size: 30rpx;
          color: #666;
          white-space: nowrap;
        }
      }
    }
    .right {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 70rpx;
    }
  }
}
</style>
