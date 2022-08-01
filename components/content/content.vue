<template>
	<view class="con">
		<u-tabs lineWidth="0" :list="list" @click="click"></u-tabs>
		<view class="listcon">
			<block v-for="(item,index) in listcon" :key="index">
				<view class="item">
					<image class="img" src="@/static/1.jpg"></image>
					<view class="con-s">
						<view class="title">
							<text class="itemT">{{item.title}}</text>
						</view>
						<view class="p">
							<text class="price">¥{{item.price}}</text>
							<text class="count">{{item.num}}人买过</text>
						</view>
						<view>
							<text class="youhui">优惠价</text>
						</view>
					</view>
				</view>
			</block>
		</view>
	</view>
</template>

<script>
	import data from '@/data/data.js'
	export default {
		name: "con",
		data() {
			return {
				listcon:data.data,
				list: [{
					name: '全部',
				}, {
					name: '零基础',
				}, {
					name: '进阶课'
				}]
			};
		},
		mounted(){
			console.log(this.listcon)
		},
		methods: {
			click(item) {
				console.log('item', item);
			}
		}
	}
</script>

<style lang="scss" scoped>
	.con {
		height: 100%;
		background-color: #ededed;
		border-radius: 10rpx;
		.listcon{
			display: flex;
			flex-wrap: wrap;
			justify-content: space-around;
		}
		.item{
			margin-top: 16rpx;
		}
		.img{
			width: 300rpx;
			height: 180rpx;
			border-radius: 20rpx;
			border-bottom: none;
		}
		.con-s{
			width: 290rpx;
			height: 120rpx;
			background-color: #fff;
			border-radius: 20rpx;
			padding: 10rpx 0 10rpx 10rpx;
		}
		.itemT{
			color: #a2a2a2;
		}
		.price{
			font-size: 28rpx;
			color: red;
		}
		.count{
			color: #ccc;
			margin-left: 30rpx;
		}
		.youhui{
			border: 1rpx solid red;
			color: red;
			font-size: 20rpx;
			padding: 2rpx;
		}
	}
</style>
