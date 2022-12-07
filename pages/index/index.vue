<template>
	<view class="content">
		<!-- 邀请信息 -->
		<div>
			邀请信息
		</div>
		<!-- 图片 -->
		<div class="demo-image__lazy">
		  <el-image v-for="uri in urls" :key="uri" :src="uri" lazy></el-image>
		</div>
		<!-- 地图 -->
		<view class="page-body">
			<view class="page-section page-section-gap">
				<map style="width: 100%; height: 300px;" 
				:latitude="latitude" 
				:longitude="longitude" 
				:enable-satellite="true"
				:show-location="true"
				:markers="covers">
				</map>
				
			</view>
		</view>
		<!-- 回到顶部 -->
		<el-backtop :bottom="100">
		    <div
		      style="{
		        height: 100%;
		        width: 100%;
		        background-color: #f2f5f6;
		        box-shadow: 0 0 6px rgba(0,0,0, .12);
		        text-align: center;
		        line-height: 25px;
		        color: rgb(250 25 110);
		      }"
		    >回到顶部</div>
		</el-backtop>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				urls: [
					  // './static/photo/0aizailntuDSC_3804 (2).jpg',
					  // './static/photo/0爱在旅途DSC_3804 (6).jpg',
					  '/h5/static/photo/0爱在旅途DSC_3804 (9)-tuya.jpg',
					  '/h5/static/photo/0W8A6967-tuya.jpg',
					  '/h5/static/photo/0W8A7152-tuya.jpg',
					  '/h5/static/photo/爱无止境DSC_3836 (5)-tuya.jpg',
					  '/h5/static/photo/爱无止境DSC_3836 (12)-tuya.jpg',
					  '/h5/static/photo/非常完美DSC_3873 (5)-tuya.jpg',
					  '/h5/static/photo/风之恋曲DSC_3646 (12)-tuya.jpg',
					  '/h5/static/photo/日光如歌DSC_3686 (11)-tuya.jpg',
					  '/h5/static/photo/喜结连理0W8A6973 (14)-tuya.jpg',
					],
				// urls: [
				// 	  {
				// 		  uri: '/h5/static/photo/0爱在旅途DSC_3804 (9)-tuya.jpg',
				// 		  class:'animate__slideOutDown',
				// 		  index: '1'
				// 	  },{
				// 		  uri: '/h5/static/photo/0W8A6967-tuya.jpg',
				// 		  class: 'animate__zoomInLeft',
				// 		  index: '2'
				// 	  },{
				// 		  uri: '/h5/static/photo/0W8A7152-tuya.jpg',
				// 		  class: 'animate__lightSpeedInRight',
				// 		  index: '3'
				// 	  }
				// 	],
				id:0, // 使用 marker点击事件 需要填写id
				title: 'map',
				latitude: 31.75801160449997,
				longitude: 107.7966499843216,
				covers: [{
					latitude: 31.75801160449997,
					longitude: 107.7966499843216,
					title: '小湾院子',
					iconPath: 'https://mapapi.qq.com/web/lbs/javascriptV2/demo/img/center.gif'
				}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin: 0% 1% 0% 1%;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	.page-body{
		width: 100%;
	}
</style>
