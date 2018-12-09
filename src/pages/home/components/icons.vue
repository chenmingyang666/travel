<template>
	<div class="icons">
		 <div class="icon" v-for="(item,index) of imgList" :key="index">
			<div class="icon-img">
				<img class="icon-img-content" :src="item.imgUrl" alt="">
			
			</div>
			<p class="icon-desc">{{item.title}}</p>
		</div>	 
		
	</div>
</template>
<script>
	export default{
		name:'HomeIcons',
		 data(){
		 	return{
		 		imgList:[{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'著名景区'
		 		},]
		 	}
		 }
	}
</script>
<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	.icons
		overflow:hidden
		height:0
		padding-bottom:50% 	
		.icon
			position:relative
			overflow:hidden
			float:left
			width:25%
			height:0
			float:left
			padding-bottom:25%
			.icon-img
				position:absolute
				left:0
				top:0
				right:0
				bottom:.24rem
				box-sizing:border-box
				padding:.1rem
				.icon-img-content
					display:block
					margin:0 auto
					height:100%
			.icon-desc
					position:absolute
					left:0
					right:0
					bottom:0
					height:.44rem
					line-height:.44rem
					text-align:center
					color:$darkTextColor
					
						
				
</style>