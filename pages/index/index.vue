<template>
	<view class="background" :style="{backgroundColor: `${bgColor}`}">
		<!-- 顶部活动图片 -->
		<view class="head" :style="{backgroundImage:`url(${headimage})`}">
			<view class="head-tag">
				音乐
			</view>
			<view class="head-tag">
				电话
			</view>
			<view class="head-tag">
				二维码
			</view>
		</view>
		<!-- 礼盒图片 -->
		<view class="box">
			<image class="box-image" :src="giftImage" mode=""></image>
		</view>
		<!-- 活动倒计时 -->
		<card title='活动倒计时'>
			<uni-countdown class='countdown' :day="1" :hour="1" :minute="59" :second="59"></uni-countdown>
		</card>
		<view class="progress">
			<view class="progress-static">
				<view>已有<text class="progress-static-red">11</text>人参与</view>
				<view><text class="progress-static-red">1236</text>次浏览</view>
			</view>
			<progress class="progress-item" percent="40" :border-radius='10' stroke-width="20" activeColor="#FF0000" />
			<view class="progress-static">
				<view>限额<text class="progress-static-red">1000</text>人</view>
				<view>进度<text class="progress-static-red">40</text>%</view>
			</view>
		</view>
		<!-- 奖品展示 -->
		<card title='奖品展示'>
			<view class="bonus">

			</view>
		</card>
		<view class="text">
			【活动详情】
		</view>
		<view class="text">
			1.本次活动为促销活动
		</view>
		<!-- 版权 -->
		<view class="copyright">
			活动解释权归明志科技所有
		</view>
		<!-- 底部按钮 -->
		<view class="foot">
			<text class="foot-text">我的礼盒</text>
			<text class="foot-divide"></text>
			<text class="foot-text">人气排行</text>
		</view>
	</view>
</template>

<script>
	import {
		uniIcons,
		uniCountdown
	} from '@dcloudio/uni-ui'
	import card from '../../components/card.vue'
	export default {
		components: {
			uniIcons,
			uniCountdown,
			card
		},
		data() {
			return {
				bgColor: '#ff0000',
				giftImage:'/static/box.png',
				headimage: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1580665361955&di=99387e432ae004643bb5468906465d04&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F0185105c00a60da80121ab5d5f9e8e.jpg%403000w_1l_0o_100sh.jpg'
			}
		},
		onLoad() {

		},
		methods: {

		},
		onShareAppMessage() {
			return {
				title: '拆礼盒，自成一派',
				imageUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1580665521080&di=f314d1e569b3ee40e99aded2e4008c40&imgtype=0&src=http%3A%2F%2Fpic.51yuansu.com%2Fpic3%2Fcover%2F03%2F08%2F69%2F5b3f4789c7d28_610.jpg',
				desc: '帮我拆礼盒，你也可以得奖哟！'
			}
		}
	}
</script>

<style>
	.background{
		padding-bottom: 40upx;
	}
	.head {
		display: flex;
		flex-direction: column;
		align-content: flex-end;
		align-items: flex-end;
		width: 750upx;
		height: 400upx;
		padding-top: 60upx;
		background-repeat: no-repeat;
		background-size: cover;

	}

	.head-tag {
		background-color: #F0AD4E;
		color: #FFFFFF;
		border-bottom-left-radius: 10px;
		border-top-left-radius: 10px;
		margin: 15upx 0;
		width: 80upx;
		height: 32upx;
		font-size: 24upx;
		line-height: 32upx;
		text-align: center
	}

	.box {
		display: flex;
		flex-direction: column;
		align-content: center;
		align-items: center;
		justify-content: center;
		width: 750upx;
		height: 500upx;
		background-repeat: no-repeat;
		background-size: cover;
	}

	.box-image {
		height: 250upx;
		width: 300upx;
	}


	.countdown {
		font-size: 50upx;
	}

	.progress {
		margin: 30upx;
		padding: 30upx;
		width: 630upx;
		border-radius: 10upx;
		background-color: #FFFFFF;
	}

	.progress-static {
		display: flex;
		justify-content: space-between;
	}

	.progress-static-red {
		color: red
	}

	.progress-item {
		margin: 50upx 0;
	}

	.bonus {
		height: 100upx;
	}

	.text {
		margin: 30upx;
		width: 690upx;
		font-size: 28upx;
		color: #FFFFFF;
	}

	.copyright {
		width: 750upx;
		text-align: center;
		font-size: 28upx;
		color: #FFFFFF;
	}

	.foot {
		margin: 40upx 40upx 0 40upx;
		width: 670upx;
		height: 80upx;
		background-color: #F0AD4E;
		display: flex;
		align-items: center;
		align-content: center;
		border-radius: 10upx;
	}

	.foot-text {
		flex: 1;
		color: #FFFFFF;
		font-size: 32upx;
		line-height: 80upx;
		text-align: center;
	}

	.foot-divide {
		width: 1px;
		height: 40upx;
		border-left: 1px solid #FFFFFF;
	}
</style>
