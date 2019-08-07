<template>
	<view>
		<!--banner-->
		<view class="kyle-padding-sm ">
			<image class="kyle-1-1 kyle-radius banner-img" :src="banner.url"></image>
		</view>
		<view class="kyle-split"></view>
		<!--分类-->
		<view class="uni-flex uni-row">
			<view class="kyle-5-1 kyle-center" v-for="icon in icons" :key="icon.id">
				<view>
					<image class="kyle-2-1 kyle-radius banner-icon" 
						:src="icon.url"></image>
				</view>
				<view>
					<text>{{icon.title}}</text>
				</view>
			</view>
		</view>
		<view class="kyle-split"></view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				banner:{id:1,url:"../../static/banner/banner1.jpg"},
				icons:[
					{id:1,url:"../../static/logo.png",title:"单身期"},
					{id:2,url:"../../static/logo.png",title:"追求期"},
					{id:3,url:"../../static/logo.png",title:"恋爱期"},
					{id:4,url:"../../static/logo.png",title:"失恋期"},
					{id:5,url:"../../static/logo.png",title:"婚后期"}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.banner-img{
		height: 200upx;
	}
	.banner-icon{
		height: 50upx;
	}
</style>
