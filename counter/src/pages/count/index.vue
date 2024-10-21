<template>
	<view class="app-content">
		<input type="text" class="input" v-model="title" placeholder="自定义文件名" />
	</view>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const title = ref('');
</script>

<style lang="scss" scoped>
.app-content {
	margin: 30rpx;
}
.input {
	padding: 0 36rpx;
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
</style>
