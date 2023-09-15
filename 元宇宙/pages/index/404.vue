<template>
	<view class="NotFind">
		<img class='noResult' src="@/static/icon-no-result.png" alt="">
		<span>未搜索到您的证书</span>
		<button @click="returnIndex">返回</button>
		<img class='logo' src="@/static/logo-suwiof.png">
	</view>
</template>

<script>
	export default{
		methods:{
			returnIndex(){
				uni.navigateBack(1)
			}
		}
	}
</script>

<style lang="scss">
	.NotFind{
		width: 100%;
		text-align: center;
		padding-top: 250rpx;
		font-size: 26rpx;
		color: #333;
		.noResult{
			width: 250rpx;
			height: 250rpx;
		}
		span{
			margin-top: 20rpx;
			display: block;
		}
		button{
			margin-top: 20rpx;
			line-height: 60rpx;
			width: 150rpx;
			height: 60rpx;
		}
		.logo{
			margin-top: 720rpx;
			width: 250rpx;
			height: 44rpx;
		}
		
	}
</style>