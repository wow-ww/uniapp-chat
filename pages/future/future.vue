<template>
	<view class="nav">
		<navigator url="/pages/login/login" open-type="redirect" hover-class="other-navigator-hover">
			<button type="default">退出</button>
		</navigator>
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

<style lang="less">
	@nav-height: var(--status-bar-height);
	.border {
		border: 1px red solid;
	}
	.flex-c {
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		align-items: center;
	}
	.nav {
		width: 100%;
		height: calc(@nav-height + 60px);
		// .border();
		.flex-c();
	}
</style>
