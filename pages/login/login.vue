<template>
	<view>
		<view class="logo">
			<image src="../../static/image/login/火.png" style="width: 144px; height: 75px;"/>
		</view>
		<view class="content">
			<text class="login-text">登录</text>
			<input type="nickname" :value="user_name" placeholder="请输入用户名" class="login-input" />
			<input password="true" :value="pwd" placeholder="请输入密码" class="login-input" />
			<button class="login-btn" @click="loginClick()">登录</button>
			<button class="register-btn" @click="registerClick()">注册</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				pwd: '',
				user_name: ''
			}
		},
		methods: {
			loginClick() {
				console.log("登录按钮被点击！");
				this.toIndex();
			},
			registerClick() {
				console.log("登录界面注册按钮被点击！");
				this.register();
			},
			toIndex() {
				console.log("跳转tabBar 首页");
				uni.switchTab({
					url: '/pages/index/index'
				});
			},
			register() {
				uni.navigateTo({
					url: '/pages/register/register'
				});
			}
		}
	}
</script>

<style lang="less">
	@nav-height: var(--status-bar-height);
	.border {
		border: 1px red solid;
	}
	.flex-r {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: flex-end;
	}
	.flex-c {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
	}
	.logo {
		width: 100%;
		height: calc(@nav-height + 220px);
		// .border();
		.flex-r();
	}
	.content {
		.flex-c();
		padding: 48px 28px 0 28px;
	}
	.login-text {
		height: 25px;
		line-height: 25px;
		// padding-right: 28px;
		font-size: 28px;
		// .border();
	}
	.register-text {
		.login-text();
	}
	.login-input {
		border-bottom: 1px rgba(39,40,50,0.08) solid;
		width: 100%;
		height: 50px;
		margin-top: 20px;
	}
	.login-btn {
		width: 65%;
		margin-top: 40px;
		background-color: #FFE431;
		font-weight: 700;
		color: #fff;
		border-radius: 20px;
	}
	.register-btn {
		.login-btn();
		border: 2px #FFE431 solid;
		color: #FFE431;
		background-color: unset;
		margin-top: 20px;
	}
</style>
