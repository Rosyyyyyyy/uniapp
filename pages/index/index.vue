<template>
	<view class="content">
		<MyNav></MyNav>
		<Content></Content>
	</view>
</template>

<script>
	import MyNav from '@/components/MyNav/MyNav.vue'
	import Content from '@/components/content/content.vue'
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		components:{
			MyNav,
			Content
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	
</style>
