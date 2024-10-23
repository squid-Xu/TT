<template>
	<view class="app-content">
		<input type="text" class="folder" v-model="title" placeholder="自定义文件名" />
		<div class="figure">{{ count }}</div>
		<div class="operation">
			<div class="controls flex-1">
				<div class="box flex-1">
					<div class="circle bg-1">
						<img class="icon" src="../../static/set.png" alt="" />
					</div>
					<div class="title">设置</div>
				</div>
				<div class="box flex-1">
					<div class="circle bg-3">
						<img class="icon" src="../../static/save.png" alt="" />
					</div>
					<div class="title">保存</div>
				</div>
				<div class="box flex-1">
					<div class="circle bg-2">
						<img class="icon" src="../../static/refer.png" alt="" />
					</div>
					<div class="title">重置</div>
				</div>
			</div>
			<div class="blank"></div>
			<div class="controls flex-2">
				<div class="box flex-2">
					<div class="circle bg-4">
						<img class="icon" src="../../static/minus.png" alt="" />
					</div>
					<div class="title">每次减一</div>
				</div>
				<div class="box flex-3">
					<div class="circle bg-5">
						<img class="icon" src="../../static/add.png" alt="" />
					</div>
					<div class="title">每次加一</div>
				</div>
			</div>
		</div>
	</view>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const title = ref('');
const count = ref<number>(0);
</script>

<style lang="scss" scoped>
.app-content {
	height: 100vh;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	margin: 0 30rpx;
}
//文件夹
.folder {
	flex-shrink: 0;
	padding: 0 36rpx;
	margin: 30rpx 0;
	height: 84rpx;
	border-radius: 10rpx;
	border: 1rpx solid #dddddd;
	background: #f8f8f8;
	box-shadow: 0px 3px 6px 0px rgba(242, 242, 242, 0.7);
	&::placeholder {
		font-size: 28rpx;
		color: #999999;
	}
}
// 数字区域
.figure {
	flex-shrink: 0;
	margin: 50rpx 0 50rpx;
	text-align: right;
	font-family: PingFang SC;
	font-weight: bold;
	font-size: 150rpx;
	color: #000000;
}
// 操作区间
.operation {
	flex: 1;
	display: flex;
	// flex-direction: row-reverse;
	.controls {
		display: flex;
		flex-direction: column;
	}
	.box {
		margin-bottom: 30rpx;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		border-radius: 10rpx;
		border: 1rpx solid #dddddd;
		background: #f8f8f8;
		box-shadow: 0px 3px 6px 0px rgba(242, 242, 242, 0.7);
		.circle {
			width: 100rpx;
			height: 100rpx;
			display: flex;
			align-items: center;
			justify-content: center;
			border-radius: 50%;
			.icon {
				width: 40rpx;
				height: 40rpx;
			}
		}
		.title {
			font-family: PingFang SC;
			font-weight: 500;
			font-size: 34rpx;
			color: #333333;
			padding-top: 30rpx;
		}
	}
}
.flex-1 {
	flex: 1;
}
.flex-2 {
	flex: 2;
}
.flex-3 {
	flex: 3;
}
.bg-1 {
	background: #37d6d0;
}
.bg-2 {
	background: #ff7777;
}
.bg-3 {
	background: #38b6ff;
}
.bg-4 {
	background: #ffa145;
}
.bg-5 {
	background: #3489ff;
}
</style>
