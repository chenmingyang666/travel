<template>
	<div class="icons">
	<swiper>
     <swiper-slide v-for="(page,index) of pages" :key="index">
         <div class="icon"  v-for="(item,index) of page" :key="index">
			<div class="icon-img">
		<img class="icon-img-content" :src="item.imgUrl" alt="">
			
			</div>
			<p class="icon-desc">{{item.title}}</p>
		</div>	
      </swiper-slide>
    
      
  </swiper>
		 
		
	</div>
</template>
<script>
	export default{
		name:'HomeIcons',
		 data(){
		 	return{
		 		imgList:[{
		 			imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/94/A9/Cii-T1hmH2yIURNDAAAJyfc0kUYAAGMPAP_79EAAAnh702.png',
		 			title:'全球wifi'
		 		},{
		 			imgUrl:'https://m.tuniucdn.com/fb2/t1/G5/M00/BA/9B/Cii-s1rQQK-IRf8xAAAIOKU8KZoAAFjGAP_93sAAAiF451.png',
		 			title:'目的地参团'
		 		},{
		 			imgUrl:'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
		 			title:'婚纱旅拍'
		 		},{
		 			imgUrl:'https://m3.tuniucdn.com/fb2/t1/G4/M00/2B/43/Cii_J1myMKOIa59DAAAEk3iRAL8AAA1twP_-1UAAASr274.png',
		 			title:'主题游'
		 		},{
		 			imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/56/A5/Cii-U1iFo6eIaZs0AAAGZNY4WVMAAHINQP_-V8AAAah882.png',
		 			title:'目的地大全'
		 		},{
		 			imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/84/64/Cii-U1ir_DyIWjOQAAAMzJwlIzUAAHmAQP_8xsAAAzl573.png',
		 			title:'蜜月游'
		 		},{
		 			imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/56/7D/Cii9EViFfe2IVXYOAAAJ0Vcji84AAHIGQP_9XMAAAqN711.png',
		 			title:'海岛游'
		 		},{
		 			imgUrl:'https://m4.tuniucdn.com/fb2/t1/G5/M00/B5/4B/Cii-tFrMg4CINw_XAAAFOVqbjXkAAFafgP_-qYAAAVa328.png',
		 			title:'当季热玩'
		 		},{
		 			imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/F3/1C/Cii-T1iULIKIW6kBAAAFJJmHzD4AAG8NwP_-sIAAAU-443.png',
		 			title:'旅游百货'
		 		}]
		 	}
		 },
		 computed:{
		 	pages (){
		 		const pages=[]
		 		this.imgList.forEach((item,index)=>{
		 			const page=Math.floor(index / 8)
		 			if(!pages[page]){
		 				pages[page]=[]
		 			}
		 			pages[page].push(item)
		 		})
		 		return pages
		 	}
		 }
	}
</script>
<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	@import '~styles/mixins.styl'
	.icons >>>.swiper-container
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
					ellipsis()
					
						
				
</style>