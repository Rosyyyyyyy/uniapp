<template>
	<view class="box">
		<view class="nav">
			<view class="mu">慕课网</view>
			<view>
				<text>下载APP</text>
				<text>登录</text>
			</view>
		</view>
		<u-tabs :list="list1" @click="click1"></u-tabs>
		<u-tabs  lineWidth="0" :list="list2" @click="click2"></u-tabs>
	</view>
</template>

<script>
	export default {
		name: "MyNav",
		data() {
			return {
				list1: [{
					name: '首页',
				}, {
					name: '免费课',
				}, {
					name: '实战课'
				}, {
					name: '体系课'
				}],
				list2: [{
					name: '专栏',
				}, {
					name: '手机',
				}, {
					name: '备课教程'
				}],
			}
		},
		methods: {
			click1(item) {
				console.log('item', item);
			},
			click2(item) {
				console.log('item', item);
			}
		}
	}
</script>

<style lang="scss">
	.nav {
		.mu {
			font-size: 32rpx;
		}

		display: flex;
		justify-content: space-between;
		align-items: center;

		text {
			border: 1rpx solid #ccc;
			border-radius: 20rpx;
		}
	}
</style>
