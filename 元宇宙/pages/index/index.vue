<template>
	<view class="content">
		<view class="banner">
			<img src="@/static/banner-search.jpg">
		</view>
		<view class="nav">
			<view class="organize">
				<img src="@/static/icon-org.png" mode="aspectFit">
				<span>发证机构：??????????????????????</span>
			</view>
			<view class="search-input-view">
					<input class='search-input'type="text" placeholder="请输入身份证号查询" v-model='inputData'>
					<img src="@/static/icon-search.png" @click='search'>
			</view>
			<view class="add" @click="addMember">
				<button>添加成员</button>
			</view>
			<scroll-view class="footer" scroll-y="true">
				<img src="@/static/logo-suwiof.png">
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				inputData:'',
				myUrl:'http://localhost:3000/search'
			}
		},
		methods: {
            search(){
				uni.request({
					url:this.myUrl,
					method:'GET',
					data:{
					    userId:this.inputData
					},
					success(res) {
						if(res.data.code==='1'){//成功
							uni.navigateTo({
								url:'detail'
							})
						}else{
							uni.navigateTo({
								url:'404'
							})
						}
						
					}
				})
			},
			addMember(){
				uni.navigateTo({
					url:'/pages/index/addMember'
				})
			}
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
		position: relative;
		margin-top: -40px;
		border-radius: 10px 10px 0px 0px;
		background-color: white;
		padding-top: 25rpx;
		.organize{
			width: 100%;
			// background-color: gold;
			display: flex;
			font-size: 28rpx;
			line-height: 44rpx;
			justify-content: center;
			color: #787B84;
			img{
				width: 44rpx;
				height: 44rpx;
			}
			span{
				word-break: break-all;
			}
		}
		.search-input-view{
			position: relative;
			width: 100%;
			font-weight: 400;
			font-size: 14px;
			line-height: 22px;
			text-align: center;
			padding-top: 50rpx;
			img{
				position: absolute;
				width: 48rpx;
				height: 48rpx;
				transform: translate(-50rpx,5rpx);
				z-index: 99;
			}
			.search-input{
				border-radius: 5px;
				width: 500rpx;
				height:60rpx;
				border: 4rpx solid #336CC2;
				line-height: 60rpx;
				padding: 0px 20rpx 0px 20rpx;
				display: inline-block;
				box-sizing: border-box;
				vertical-align: middle;
				text-align: left;
			}
		}
		.add{
		   margin-top: 50rpx;
		   width: 100%;
		   display: flex;
		   justify-content: center;
		   button{
			   display: inline-block;
			   color: #787B84;
		   }	
		}
	}
	.footer{
		width: 100%;
		text-align: center;
		img{
			margin-top: 700rpx;
			width: 250rpx;
			height: 44rpx;
		}
	}
	
</style>
