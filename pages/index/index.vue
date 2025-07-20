<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<MyButton text="测试按钮" @click="onBtnClick" />
		<MyCard title="easycom卡片">
			<text>这是通过easycom自动引入的卡片组件内容。</text>
		</MyCard>
	</view>
</template>

<script>
import MyButton from '@/components/MyButton.vue'
export default {
	components: {
		MyButton
	},
	data() {
		return {
			title: 'Hello'
		}
	},
	onLoad() {

	},
	methods: {
		onBtnClick() {
			uni.showToast({ title: '按钮被点击了', icon: 'none' });
		}
	}
}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
