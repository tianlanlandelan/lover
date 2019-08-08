<template>
	<view>
		<uni-card v-for="list in dialogueList" :key="list.groupId">
			<view v-for="info in list.list" :key="info.id">
				<view class="uni-flex uni-row">
					<view class="kyle-8-1 kyle-center">
						<image src="../static/icon/nan.png" v-if="info.gender==0"></image>
						<image src="../static/icon/nv.png" v-if="info.gender==1"></image>
					</view>
					<view class="kyle-4-3">
						<text>{{info.content}}</text>
					</view>
					<view class="kyle-8-1 kyle-center">
						<image  src="../static/icon/copy.png" @click="setClipboard(info.content)"></image>
					</view>
				</view>
			</view>
		</uni-card>
	</view>
</template>

<script>
	import uniCard from '@/components/uni-card/uni-card.vue'
	
	export default {
		//页面加载时执行的方法，option为object类型，会序列化上个页面传递的参数
		onLoad: function (option) { 
			//打印出上个页面传递的参数
			console.log(option.typeId,option.typeName); 
			//设置导航栏标题
			uni.setNavigationBarTitle({
				title: option.typeName
			});
			//TODO 发送请求，获取页面显示数据
			
		},
		components: {
			uniCard
		},
		data() {
			return {
				title:'',
				dialogueList:[
					{groupId:1,list:[
						{id:1,gender:1,content:"你好笨啊！"},
						{id:2,gender:0,content:"所以上帝让你下来拯救我了"}
					]},
					{groupId:2,list:[
						{id:5,gender:1,content:"你好讨厌！"},
						{id:6,gender:0,content:"你知道中国女人跟国外女人最大的不同在哪吗？"},
						{id:7,gender:1,content:"有什么不同"},
						{id:8,gender:0,content:"外国女人表达爱意是说我爱你，中国女人是说你真讨厌"}
					]}
				]
			}
		},
		methods:{
			setClipboard(text){
				uni.setClipboardData({
					data: text,
					success: () => {
						console.log(text);
					},
				});
			}
		}
	}
</script>

<style>
	image{
		width: 40upx;
		height: 40upx;
	}
</style>
