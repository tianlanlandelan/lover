<template>
	<view>
		<!--banner-->
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
		<view class="kyle-split"></view>
		<!--搜索-->
		<view class="uni-flex uni-row view-search view-margin">
			<view class="left kyle-4-3">
				<input class="uni-input" confirm-type="search" 
				placeholder="请输入关键字搜索聊天话术" />
			</view>
			<view class="right kyle-center kyle-4-1">
				<button type="warn" size="mini">搜索</button>
			</view>		
		</view>
		<view class="kyle-split"></view>
		<!--简介-->
		<view class="uni-flex uni-row kyle-padding">
			<view class="kyle-2-1">
				<text>一款优秀的话术搜索代聊软件</text>
			</view>
			<view class="kyle-2-1 kyle-right">
				<text>今日新增511条话术</text>
			</view>		
		</view>
		<view v-for="menu in menus" :key="menu.title">
			<view class="kyle-split"></view>
			<view class="kyle-padding">
				<text>{{menu.title}}</text><text>|</text><text>{{menu.content}}</text>
			</view>
			<view class="kyle-inline kyle-margin-sm" v-for="sub in menu.subTitle" :key="sub.id">
				<uni-tag :text="sub.name" type="primary" />
			</view>	
		</view>
		
		<view class="kyle-footer"></view>
	</view>
</template>
<script>
	import uniTag from '@/components/uni-tag/uni-tag.vue'
	export default {
		data() {
			return {
				banners:[
					"../../static/banner/banner1.jpg",
					"../../static/banner/banner2.jpg",
					"../../static/banner/banner3.jpg"
				],
				menus:[
                    {title:"开场",content:"尬聊只需搜一搜",
                        subTitle:[
									{id:11,name:"搭讪开场"},
									{id:12,name:"话题重新开始"},
									{id:13,name:"表情话术"},
									{id:14,name:"趣味搭讪"},
									{id:15,name:"勾起好奇"}
								],
					},
                    {title:"情绪",content:"他/她的情绪我知道",
                        subTitle:[
									{id:21,name:"幽默聊天"},
									{id:22,name:"共谋与赞美"},
									{id:23,name:"调侃"},
									{id:24,name:"自恋"},
									{id:25,name:"影视综艺梗"},
									{id:26,name:"打情骂俏"}
								],
					},
                    {title:"聊天",content:"天南海北都有料",
                        subTitle:[
									{id:31,name:"初聊互动"},
									{id:32,name:"价值型聊天"},
									{id:33,name:"冷读术"},
									{id:34,name:"话块连情"},
									{id:35,name:"框架筛选"},
									{id:36,name:"高价值展示"},
									{id:37,name:"情感链接"},
									{id:38,name:"共鸣故事"},
									{id:39,name:"异议处理"}
                        ]},
                    {title:"升级",content:"拾火添柴有妙招",
						subTitle:[
									{id:41,name:"恋爱调情"},
									{id:42,name:"暧昧话术"},
									{id:43,name:"关系提高"},
									{id:44,name:"表达兴趣"},
									{id:45,name:"合约恋人"},
									{id:46,name:"情感波动"}
								],
					},
                    {title:"邀约",content:"亲爱的我们约会吧",
						subTitle:[
									{id:51,name:"模糊邀约"},
									{id:52,name:"邀约话术"},
									{id:53,name:"速约模板"},
									{id:54,name:"预期建立"},
									{id:55,name:"促成邀约"}
								],
					},
                    {title:"约会",content:"共度美好时光",
						subTitle:[
									{id:61,name:"现场聊天交流"},
									{id:62,name:"互动与游戏"},
									{id:63,name:"聊天模板"},
									{id:64,name:"颜色星座手相"},
									{id:65,name:"约会套路"}
								],
					}
                ]
			}
		},
		methods: {
			
		},
		components:{uniTag}
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
	.view-search {
		height: 100upx;
		width:100%;
	}
	input{
		border-radius:10upx;
		line-height: 80upx;
	}
	.right button{
		line-height: 80upx;
	}
	.sub-text{
		height: 80upx;
		line-height: 80upx;
	}
	.flex-item {
		width: 33.3%;
		height: 200upx;
		line-height: 200upx;
	}
</style>
