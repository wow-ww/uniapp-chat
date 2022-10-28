<template>
	<view>
		<view class="nav">
			<text @click="backLogin()">返回</text>
		</view>
		<view class="content">
			<text class="register-text">注册</text>
			<input :value="user_name" placeholder="请输入用户名" class="login-input" />
			<input password="true" :value="pwd" placeholder="请输入密码" class="login-input" />
			<input password="true" :value="confirm_pwd" placeholder="请再次输入密码" class="login-input"></input>
			<button class="register-btn" @click="registerClick()">注册</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				user_name: '',
				pwd: '',
				confirm_pwd: ''
			}
		},
		methods: {
			registerClick() {
				console.log("登录界面注册按钮被点击！");
				this.register();
			},
			register() {
				console.log("注册成功！请登录！");
				uni.navigateBack();
			},
			backLogin() {
				console.log("返回登录！");
				uni.navigateBack();
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
		justify-content: flex-start;
		align-items: center;
	}
	.flex-c {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
	}
	.nav {
		width: 100%;
		height: calc(@nav-height + 80px);
		padding: 0 0 0 28px;
		font-size: 18px;
		// .border();
		.flex-r();
	}
	.content {
		.flex-c();
		padding: 25% 28px 0 28px;
		// transform: translateY(-50%);
		// .border();
	}
	.register-text {
		height: 25px;
		line-height: 25px;
		// padding-right: 28px;
		font-size: 28px;
		// .border();
	}
	.login-input {
		border-bottom: 1px rgba(39,40,50,0.08) solid;
		width: 100%;
		height: 50px;
		margin-top: 20px;
	}
	.register-btn {
		width: 65%;
		margin-top: 40px;
		font-weight: 700;
		color: #fff;
		border-radius: 20px;
		border: 2px #FFE431 solid;
		color: #FFE431;
		background-color: #fff;
	}
</style>
