<template>
	<view>
		<view class="card">
			<view class="card-title">
				{{title}}
			</view>
			<view class="card-content">
				<slot></slot>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:'card',
		props:{
			title:{
				type:String,
				default:'项目标题'
			}
		},
		data() {
			return {

			};
		}
	}
</script>

<style>
	.card {
		margin: 30upx;
		width: 690upx;
	}

	.card-title {
		background-color: #F0AD4E;
		color: #FFFFFF;
		text-align: center;
		font-size: 32upx;
		border-radius: 10upx 10upx 0 0;
		height: 80upx;
		line-height: 80upx;
	}

	.card-content {
		display: flex;
		justify-content: center;
		align-items: center;
		align-content: center;
		border-radius: 0 0 10upx 10upx;
		background-color: #FFFFFF;

	}
</style>
