<template>
	<view>
		<view class="nav">
			<text class="login-text">注册</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
.nav {
	display: flex;
	flex-direction: row;
	justify-content: flex-end;
	align-items: flex-end;
	width: 100%;
	height: calc(var(--status-bar-height) + 35px);
	border: 1px red solid;
}
.login-text {
	height: 25px;
	line-height: 25px;
	padding-right: 28px;
	font-size: 18px;
	border: 1px red solid;
}
</style>
