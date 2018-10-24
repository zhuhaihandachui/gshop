<template>
	<div>
		<div class="footguider">
			<div class="guide_item" :class="{on: '/msite'===this.$route.path}" @click="goTo('/msite')">
				<span>
					<i class="iconfont icon-waimai"></i>
				</span>
				<span>外卖</span>
			</div>
			<div class="guide_item" :class="{on: '/search'===this.$route.path}" @click="goTo('/search')">
				<span>
					<i class="iconfont icon-search"></i>
				</span>
				<span>搜索</span>
			</div>
			<div class="guide_item" :class="{on: '/order'===this.$route.path}" @click="goTo('/order')">
				<span>
					<i class="iconfont icon-dingdan"></i>
				</span>
				<span>订单</span>
			</div>
			<div class="guide_item" :class="{on: '/profile'===this.$route.path}" @click="goTo('/profile')">
				<span>
					<i class="iconfont icon-geren"></i>
				</span>
				<span>我的</span>
			</div>
		</div>		
	</div>
</template>

<script>
	export default {
		methods: {
			goTo(page){
				this.$router.replace(page);
			}
		}
	}

</script>
<style lang="stylus" rel="stylesheet/stylus">
	@import "../../common/stylus/mixins.styl"
	.footguider
		top-border-1px(#e4e4e4)
		position fixed
		left 0
		bottom 0
		width 100%
		height 50px
		display flex
		.guide_item
			display flex
			background-color #fff
			flex 1
			flex-direction column
			justify-content center
			align-items center
			&.on
				color #02a774
			span
				font-size 12px
				margin-top 2px
				margin-bottom 2px
				.iconfont
					font-size 22px
</style>