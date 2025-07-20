<template>
  <view class="my-card">
    <view class="my-card-title">{{ title }}</view>
    <view class="my-card-content">
      <slot>这里是卡片内容</slot>
    </view>
  </view>
</template>

<script>
export default {
  name: 'MyCard',
  props: {
    title: {
      type: String,
      default: '卡片标题'
    }
  }
}
</script>

<style scoped>
.my-card {
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.06);
  padding: 20rpx;
  margin: 20rpx;
}
.my-card-title {
  font-size: 32rpx;
  font-weight: bold;
  margin-bottom: 16rpx;
}
.my-card-content {
  font-size: 28rpx;
  color: #666;
}
</style> 