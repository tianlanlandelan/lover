<template>
	<view>
		 
		 <view class="uni-common-mt" style="background:#FFF; padding:20rpx;">
                <rich-text :nodes="strings"></rich-text>
         </view>
	</view>
</template>

<script>
	export default {
		onLoad: function (option) { 
			//打印出上个页面传递的参数
			console.log(option.id,option.title); 
			//设置导航栏标题
			uni.setNavigationBarTitle({
				title: option.title
			});
			//TODO 发送请求，获取页面显示数据
			
		},
		data(){
			return{
				strings:'<div style="text-align:center;"><img src="https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/uni@2x.png"/><p>这是文章内容</p></div>'
			}
		}
	}
</script>

<style>
</style>
