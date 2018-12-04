<template>
	<div class="header">
		 <div class="header-left">返回</div>
		 <div class="header-input">输入城市景点主题</div>
		 <div class="header-right">城市</div>
	</div>
</template>
<script>
	export default{
		name:'HomeHeader'
	}
</script>
<style lang="stylus" scoped>
	.header
		display:flex
		line-height: 0.86rem
		background:#00bcd4
		color:#fff
		.header-left
			width:.64rem
			float:left
		.header-input
			flex:1	
			margin:.12rem 0 0 .2rem
			height:.64rem
			line-height:.64rem
			background:#fff
			border-radius:5px
			color:#ccc
		.header-right
			 width:1.24rem
			 float:right
			 text-align:center
</style>