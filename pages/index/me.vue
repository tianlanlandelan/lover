<template>
	<view>
		<view class="kyle-padding kyle-radius">		
			<uni-list>
				<uni-list-item title="我的收藏" thumb="../../static/bar/school1.png" />
				<uni-list-item title="客服反馈" thumb="../../static/bar/school1.png" />
				<uni-list-item title="账号安全" thumb="../../static/bar/school1.png" />
				<uni-list-item title="使用帮助" thumb="../../static/bar/school1.png" />
				<uni-list-item title="设置" thumb="../../static/bar/school1.png" />
			</uni-list>
		</view>
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
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>