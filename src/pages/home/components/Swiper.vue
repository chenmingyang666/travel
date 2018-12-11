<template>
<div class="wrapper">
	<swiper :options="swiperOption" v-if="swiperList.length>0">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    <!-- <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div> -->
    <!-- <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
  </swiper>
</div>
	 
</template>
<script>
	export default{
		name:'HomeSwiper',
		data (){
			return {
				swiperOption:{
					pagination : '.swiper-pagination',
					 
				},
				swiperList:[{
					id:'001',
					imgUrl:'http://dimg04.c-ctrip.com/images/700s0z000000mqyqyD43D_640_128_25.jpg'
				},{
					id:'002',
					imgUrl:'http://dimg04.c-ctrip.com/images/700g0z000000mkz5sF0EC_640_128_25.jpg'
				},{
					id:'003',
					imgUrl:'http://dimg04.c-ctrip.com/images/700g0z000000mkz5sF0EC_640_128_25.jpg'
				},{
					id:'004',
					imgUrl:'http://dimg04.c-ctrip.com/images/700e0z000000mkpfgC2B1_640_128_25.jpg'
				},{
					id:'005',
					imgUrl:'http://dimg04.c-ctrip.com/images/700u0z000000mkqtf7736_640_128_25.jpg'
				}]
			}
		}
		 
	}
</script>
<style lang="stylus" scoped>
	.wrapper>>>.swiper-pagination-bullet-active
			background:white
	.wrapper
		overflow:hidden
		width:100%
		height:0
		// 高:宽
		padding-bottom:20%
		background:#eee
		.swiper-img
			width:100%
</style>