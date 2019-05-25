<template>
	<div class="icons">
	<swiper :options="swiperOption" v-if="showSwiper">
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
		props:{
			icons:Array
		},
		 data(){
		 	return{
		 	swiperOption:{
					
					autoplay:false
				}	
		 	}
		 },
		 computed:{
			
			showSwiper(){
				return this.icons.length
			},
		 	pages (){
		 		const pages=[]
		 		this.icons.forEach((item,index)=>{
		 			const page=Math.floor(index / 8)
		 			console.log(page)
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
	.icons
		margin-top:.1rem	
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