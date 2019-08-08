<template>
	<view>
		<view class="kyle-1-1">
			<swiper class="swiper" 
			 indicator-dots="true" 
			 autoplay="true" 
			 interval="2000" 
			 duration="500">
				<swiper-item v-for="banner in banners" :key="banner">
					<view class="swiper-item">
						<image class="kyle-1-1" :src="banner"></image>
					</view>
				</swiper-item>
			</swiper>
		</view>
		<view class="kyle-padding">
			<uni-list>
				<uni-list-item  
				    :show-arrow="false"
					:thumb="icon" 
					v-for="story in stories"  
					:key="story.title" 
					:note="story.title" 
				/>
			</uni-list>
			
		</view>
		<view class="kyle-center">
			<button class="kyle-4-3 kyle-radius" type="warn">开通VIP可查看更多</button>
		</view>
		<view class="kyle-footer"></view>
	</view>
</template>

<script>
	import uniList from '@/components/uni-list/uni-list.vue'
	import uniListItem from '@/components/uni-list-item/uni-list-item.vue'
	
	export default {
		components: {
			uniList,
			uniListItem
		},
		data() {
			return {
				banners:[
					"../../static/banner/banner1.jpg",
					"../../static/banner/banner2.jpg",
					"../../static/banner/banner3.jpg"
				],
				icon:"../../static/icon/wechat.png",
				stories:[
					{title:"舔狗式撩甜妹子，没被拉黑反而变男票"},
					{title:"女票突然发起命题，强大的求生欲使我做出如下回答"},
					{title:"不讨人厌的热情邀约，拿下了女神的初恋"},
					{title:"五种撩妹子套路，学会一半随便脱单"},
					{title:"她不是成都小甜甜，却被我撩成了蹦迪CP"},
					{title:"搭上狂野小懒猫，知心人设让她主动黏上我"},
					{title:"80后姐姐嫌我嫩，一番深聊后让她对我改观"},
					{title:"柴犬表情包敲开话题，一步步走进她的内心"},
					{title:"加到甜美妹纸，每夜一句晚安拿下她"},
					{title:"从哈喽到老公，我和她只聊了一个小时"},
					{title:"舔狗式撩甜妹子 没被拉黑反而变男票"},
					{title:"女票突然发起命题 强大的求生欲使我做出如下回答"},
					{title:"不讨人厌的热情邀约 拿下了女神的初恋"},
					{title:"五种撩妹子套路学会一半随便脱单"},
					{title:"她不是成都小甜甜 却被我撩成了蹦迪CP"},
					{title:"搭上狂野小懒猫 知心人设让她主动黏上我"},
					{title:"80后姐姐嫌我嫩 一番深聊后让她对我改观"},
					{title:"柴犬表情包敲开话题 一步步走进她的内心"},
					{title:"加到甜美妹纸 每夜一句晚安拿下她"},
					{title:"从哈喽到老公 我和她只聊了一个小时"}
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
	.swiper {
		height: 300upx;
	}
	.swiper-item {
		display: block;
		height: 300upx;
		line-height: 300upx;
		text-align: center;
	}
	.image{
		width:100%;
	}
</style>
