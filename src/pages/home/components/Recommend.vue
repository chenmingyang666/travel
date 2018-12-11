<template>
	<div>
		<div class="title">强烈推荐</div>
			<ul>
				<li class="item border-bottom" v-for="(item,index) of recommendList" :key="item.id">
					 
						<img class="item-img" :src="item.imgUrl" alt="">
					 
					<div class="item-info">
						<p class="item-title">{{item.title}}</p>
						<p class="item-desc">{{item.desc}}</p>
						<button class="item-button">查看详情</button>
					</div>
				</li>
			</ul>	 
		
	</div>
</template>
<script>
	export default{
		name:'HomeRecommend',
		data(){
			return {
				recommendList:[{
					id:'001',
					imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/CD/C5/Cii-Tlh8mpWIMBb2AJnb_TpuDAEAAGx-AFne7gAmdwV525_w350_h0_c0_t0.jpg',
                    title:'曼谷-芭提雅-金沙岛6或7日游',
					desc:'去触摸泰国真正的样子，金沙岛珊瑚岛畅游双岛，升级一晚五星希尔顿，7天行程升级一天自由活动，参与泼水节狂欢'
				},{
					id:'002',
					imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/CD/C5/Cii-Tlh8mpWIMBb2AJnb_TpuDAEAAGx-AFne7gAmdwV525_w350_h0_c0_t0.jpg',
                    title:'曼谷-芭提雅-金沙岛6或7日游',
					desc:'去触摸泰国真正的样子，金沙岛珊瑚岛畅游双岛，升级一晚五星希尔顿，7天行程升级一天自由活动，参与泼水节狂欢'
				},{
					id:'003',
					imgUrl:'https://m.tuniucdn.com/fb2/t1/G2/M00/CD/C5/Cii-Tlh8mpWIMBb2AJnb_TpuDAEAAGx-AFne7gAmdwV525_w350_h0_c0_t0.jpg',
                    title:'曼谷-芭提雅-金沙岛6或7日游',
					desc:'去触摸泰国真正的样子，金沙岛珊瑚岛畅游双岛，升级一晚五星希尔顿，7天行程升级一天自由活动，参与泼水节狂欢'
				}]
			}
		}
	}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
	.title
		margin-top:.2rem
		line-height:.8rem
		bacground:#eee
		text-indent:.2rem
		background:#eee
	.item
		display:flex
		overflow:hidden
		height 1.9rem
		.item-img
			width:2rem
			height 2rem
			padding:.1rem
		.item-info	
			flex:1
			padding:.1rem
			min-width:0
			.item-title
				line-height:.34rem
				font-size:.32rem
				ellipsis()
			.item-desc	
				line-height:.4rem
				color:#ccc 
				ellipsis()		
			.item-button
				line-height:.44rem
				margin-top:.12rem
				color:#fff
				background:#ff9300
				padding:0 .1rem
				border-radius:.06rem
			
		
</style>