<template>
  <div>
    <div class="title">周末去哪</div>
      <ul>
        <li class="border-bottom" v-for="(item,index) of recommendList" :key="item.id">
          <div class="item-img-wrapper">
            <img class="item-img" :src="item.imgUrl" alt="">
          </div> 
            <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            
          </div> 
        </li>
      </ul>  
    
  </div>
</template>
<script>
  export default{
    name:'HomeWeekend',
    data(){
      return {
        recommendList:[{
          id:'001',
          imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/FF/11/Cii9EFdWM4eIKeFYAC0AOWDg_0UAAGa2AEADTsALQBR659_w450_h300_c1_t0_w800_h0_c0_t0.jpg',
                    title:'曼谷-芭提雅-金沙岛6或7日游',
          desc:'去触摸泰国真正的样子，金沙岛珊瑚岛畅游双岛，升级一晚五星希尔顿，7天行程升级一天自由活动，参与泼水节狂欢'
        },{
          id:'002',
          imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/FF/11/Cii9EFdWM4eIKeFYAC0AOWDg_0UAAGa2AEADTsALQBR659_w450_h300_c1_t0_w800_h0_c0_t0.jpg',
                    title:'曼谷-芭提雅-金沙岛6或7日游',
          desc:'去触摸泰国真正的样子，金沙岛珊瑚岛畅游双岛，升级一晚五星希尔顿，7天行程升级一天自由活动，参与泼水节狂欢'
        },{
          id:'003',
          imgUrl:'https://m.tuniucdn.com/fb2/t1/G1/M00/FF/11/Cii9EFdWM4eIKeFYAC0AOWDg_0UAAGa2AEADTsALQBR659_w450_h300_c1_t0_w800_h0_c0_t0.jpg',
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
    background:#eee
    text-indent:.2rem
  .item-img-wrapper
    overflow:hidden
    height:0
    padding-bottom:33%
    .item-img
      width:100%
  .item-info
    padding:.1rem
    .item-title
      line-height:.54rem
      font-size:.32rem
      ellipsis()
    .item-desc  
      line-height:.4rem
      color:#ccc 
      ellipsis()    
      
    
</style>