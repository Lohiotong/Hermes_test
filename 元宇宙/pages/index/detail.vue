<template>
	<view class="content">
		<view class="banner">
			<img src="@/static/bg-certificate.png">
		</view>
		<view class='nav'>
			<p class='item-Detail'>
				<span>名字</span>
				<span>{{name}}</span>
			</p>
			<p class='item-Detail'>
				<span>编号</span>
				<span>{{name}}</span>
			</p>
			<p class='item-Detail'>
				<span>所在组</span>
				<span>{{group}}</span>
			</p>
			<p class='item-Detail'>
				<span>岗位</span>
				<span>{{jop}}</span>
			</p>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name:'',
				id:'',
				group:'',
				jop:''
			}
		},
		methods: {
            
		}
	}
</script>

<style scoped lang="scss">
	.content{
		font-style: PingFang SC;
	}
	.banner{
		width: 100%;
		z-index: 0 !important;
		position: relative;
		img{
			width: 100%;
		}
	}
	.nav{
		width: 100%;
		// background-color: hotpink;
		z-index: 99 !important;
		color: #787B84;
		
		.item-Detail{
			margin: 40rpx 50rpx;
			span{
				display: inline-block;
				margin-right: 80rpx;
			}
		}
	}
	.footer{
		width: 100%;
		text-align: center;
		img{
			margin-top: 800rpx;
			width: 250rpx;
			height: 44rpx;
		}
	}
	
</style>
