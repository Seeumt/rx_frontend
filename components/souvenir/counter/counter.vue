<template>
	<view class="number">
		<view class="sub" @tap.stop="sub">
			<view class="icon iconfont">&#xe768;</view>
		</view>
		<view class="input">
			<input type="number" v-model="goodsInfo.number">
		</view>
		<view class="add" @tap.stop="add">
			<view class="icon iconfont">&#xe767;</view> 
		</view>
	</view>
</template>

<script>

	export default {
		methods:{
			sub(){
				
				// // 注册change事件
				// this.$emit("change");
				
				this.$emit("sub");
			},
			add(){
				// this.goodsInfo.number++;
				// // 注册change事件
				// this.$emit("change");
				
				this.$emit("add");
			}
		},
		props: {
			goodsInfo: Object
		}
	}
</script>

<style lang="scss">
	.number {
		display: flex;
		justify-content: center;
		align-items: center;

		.input {
			width: 80upx;
			height: 60upx;
			margin: 0 10upx;
			background-color: #f3f3f3;
			display: flex;
			justify-content: center;
			align-items: center;
			text-align: center;

			input {
				width: 80upx;
				height: 60upx;
				display: flex;
				justify-content: center;
				align-items: center;
				text-align: center;
				font-size: 26upx;
			}
		}

		.sub,
		.add {
			width: 60upx;
			height: 60upx;
			background-color: #f3f3f3;
			border-radius: 5upx;

			.icon {
				font-size: 30upx;
				width: 60upx;
				height: 60upx;
				display: flex;
				justify-content: center;
				align-items: center;
			}
		}
	}
</style>
