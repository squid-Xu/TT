<template>
	<view class="app-content">
		<input type="text" class="folder" v-model="title" placeholder="自定义文件名" />
		<div class="figure">{{ count }}</div>
		<div class="operation">
			<div class="controls flex-1">
				<div class="set box">
					<div class="item">
						<img class="icon" src="../../static/set.png" alt="" />
					</div>
					<div class="desc">减一</div>
				</div>
				<div class="set box">
					<div class="item">
						<img class="icon" src="../../static/minus.png" alt="" />
					</div>
					<div class="desc">减一</div>
				</div>
				<div class="set box">
					<div class="item">
						<img class="icon" src="../../static/minus.png" alt="" />
					</div>
					<div class="desc">减一</div>
				</div>
			</div>
			<div class="controls flex-2">
				<div class="minus box">
					<div class="item">
						<img class="icon" src="../../static/minus.png" alt="" />
					</div>
					<div class="desc">减一</div>
				</div>
				<div class="add box">
					<div class="item">
						<img class="icon" src="../../static/add.png" alt="" />
					</div>
					<div class="desc">减一</div>
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
	margin: 50rpx 0 50rpx;
	text-align: right;
	background-color: aquamarine;
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
	background-color: blueviolet;
	.controls {
		display: flex;
		flex-direction: column;
		padding-right: 30rpx;
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
		.item {
			width: 164rpx;
			height: 164rpx;
			display: flex;
			align-items: center;
			justify-content: center;
			background: #38b6ff;
			border-radius: 50%;
			.icon {
				width: 82rpx;
				height: 82rpx;
			}
		}
		.desc {
			font-family: PingFang SC;
			font-weight: 500;
			font-size: 34rpx;
			color: #333333;
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
.flex-4 {
	flex: 4;
}
</style>
