<template>
	<view >
		<view class="nav">
			<view class="top-left">
				<image src="../../static/image/pic/1.png" style="width: 34px;height: 34px;border-radius: 8px;"/>
			</view>
			<view class="top-mid">
				<image src="../../static/image/index/火.png" style="width: 44px;height: 21px;"/>
			</view>
			<view class="top-right">
				<image src="../../static/image/index/search.png" style="width: 26px;height: 26px;margin-right: 10px;"/>
				<image src="../../static/image/index/add group.png" style="width: 24px;height: 24px;"/>
			</view>
		</view>
		<view class="friend-list">
			<view class="friend-card">
				<view class="card-left">
					<image src="../../static/image/pic/addf.png" style="width: 48px;height: 48px;border-radius: 12px;"/>
					<text class="tip">1</text>
				</view>
				<view class="card-right">
					<view class="card-r-top">
						<text class="name">好友申请</text>
						<text class="time">05:56</text>
					</view>
					<text class="msg">请通过</text>
				</view>
			</view>
			<view class="friend-card" v-for="item in friends">
				<view class="card-left">
					<image :src="item.img_url" style="width: 48px;height: 48px;border-radius: 12px;"/>
					<text class="tip" v-if="item.num > 0">{{ item.num }}</text>
				</view>
				<view class="card-right">
					<view class="card-r-top">
						<text class="name">{{ item.name }}</text>
						<text class="time">{{ item.time }}</text>
					</view>
					<text class="msg">{{ item.msg }}</text>
				</view>
			</view>
			
<!-- 			<view class="friend-card">
				<view class="card-left">
					<image src="../../static/image/pic/2.png" style="width: 48px;height: 48px;border-radius: 12px;"/>
					<text class="tip">99</text>
				</view>
				<view class="card-right">
					<view class="card-r-top">
						<text class="name">随便</text>
						<text class="time">14:56</text>
					</view>
					<text class="msg">你好呀你好呀你好呀你好呀你你好呀你好呀你好你好呀你好呀你好好呀</text>
				</view>
			</view>
			
			<view class="friend-card">
				<view class="card-left">
					<image src="../../static/image/pic/2.png" style="width: 48px;height: 48px;border-radius: 12px;"/>
					<text class="tip">99</text>
				</view>
				<view class="card-right">
					<view class="card-r-top">
						<text class="name">name</text>
						<text class="time">time</text>
					</view>
					<text class="msg">msg</text>
				</view>
			</view>
			
			<view class="friend-card">
				<view class="card-left">
					<image src="../../static/image/pic/2.png" style="width: 48px;height: 48px;border-radius: 12px;"/>
					<text class="tip">99</text>
				</view>
				<view class="card-right">
					<view class="card-r-top">
						<text class="name">name</text>
						<text class="time">time</text>
					</view>
					<text class="msg">msg</text>
				</view>
			</view> -->
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				friends: [
					{name: "六六",img_url: "../../static/image/pic/4.png", time: "12:15", num: 62, msg: "你好呀"},
					{name: "wow",img_url: "../../static/image/pic/2.png", time: "14:56", num: 99, msg: "吃饭了嘛吃饭了嘛吃饭了嘛吃饭了嘛吃饭了嘛吃饭了嘛吃饭了嘛吃饭了嘛"},
					{name: "五五",img_url: "../../static/image/pic/3.png", time: "01:22", num: 1, msg: "睡了吗了吗睡了吗睡了吗睡了吗"},
					{name: "哦哦",img_url: "../../static/image/pic/1.png", time: "10:03", num: 20, msg: "饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗饿了吗"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"},
					{name: "以已",img_url: "../../static/image/pic/4.png", time: "19:53", num: 0, msg: "一起出去玩吧"}
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
.flex-r {
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
}
.flex-c {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
.nav {
	position: fixed;
	top: 0px;
	width: 100%;
	height: calc(var(--status-bar-height) + 46px);
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: flex-end;
	background-color: #fff;
	z-index: 1000;
	box-shadow: 0px 1px 0px 0px rgba(0,0,0,0.1);
}
.top-left {
	margin-left: 16px;
}
.top-right {
	margin-right: 16px;
}
.friend-list {
	margin-top: calc(var(--status-bar-height) + 46px);
}
.friend-card {
	width: 100%;
	height: 56px;
	display: flex;
	flex-direction: row;
	justify-content: flex-start;
	align-items: center;
	/* margin: 20px 16px 0 16px; */
	padding: 16px 16px 0 16px;
}
.friend-card:active {
	background-color: #F3F3F3;
}
.card-left {
	/* flex-grow: 1; */
	position: relative;
	margin-right: 16px;
}
.tip {
	position: absolute;
	font-size: 14px;
	width: 20px;
	top: -8px;
	left: 35px;
	background: red;
	border-radius: 110px;
	text-align: center;
	color: #fff;
}
.card-right {
	/* flex-grow: 0.86; */
	width: 300px;
	display: flex;
	flex-direction: column;
	justify-content: flex-start;
	align-items: flex-start;
	/* border: 1px solid red; */
}
.card-r-top {
	width: 100%;
	position: relative;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	margin-top: -10px;
	/* border: 1px solid red; */
}
.name {
	font-size: 18px;
	font-weight: 400;
	color: #272832;
}
.time {
	font-size: 12px;
	color: rgba(39,40,50,0.40);
	font-weight: 400;
}
.msg {
	width: 290px;
	font-size: 14px;
	color: rgba(39,40,50,0.60);
	font-weight: 400;
	/* 超出隐藏 */
  overflow: hidden;
  text-overflow: ellipsis;
	 white-space:nowrap;
/*  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical; */
}
</style>
