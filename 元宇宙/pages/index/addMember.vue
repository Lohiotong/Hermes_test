<template>
		<view class='addMember'>
			<p class='item-Detail'>
				<span>添加成员</span>
			</p>
			<p class='item-Detail'>
				<span>名字</span>
				<input type="text">
			</p>
			<p class='item-Detail'>
				<span>编号</span>
				<input type="text">
			</p>
			<p class='item-Detail'>
				<span>所在组</span>
				<input type="text">
			</p>
			<p class='item-Detail'>
				<span>岗位</span>
				<input type="text">
			</p>
			<button>添加</button>
			<view class="footer">
				<img src="@/static/logo-suwiof.png">
			</view>
		</view>
</template>

<script>
	
</script>

<style lang="scss">
	.addMember{
		
		position: absolute;
		width: 100%;
		// background-color: hotpink;
		z-index: 99 !important;
		color: #787B84;
		top: 50%;
		left: 50%;
		transform: translate(-50%,-50%);
		.item-Detail{
			margin: 40rpx 50rpx;
			span{
				display: inline-block;
				margin-right: 80rpx;
			}
		}
		.item-Detail:nth-child(4){
			margin: 40rpx 20rpx;
		}
		input{
			display: inline-block;
			border:1px solid black;
			vertical-align: middle;
		}
	    button{
			width: 250rpx;
			
		}
	}
	.footer{
		width: 100%;
		text-align: center;
		img{
			margin-top: 400rpx;
			width: 250rpx;
			height: 44rpx;
		}
	}
</style>