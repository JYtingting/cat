<template>
  <div id="app">
    <!-- 顶部header区域 -->

    <h1> hhhhhhh</h1>

  <!-- 底部tabber 区域 -->
  <div>
    <div id="footer_ct">
     <ul>
       <li v-for="(tabber, index) in tabbers" :key="index" :class="{active:index==tabber_color}"  @click="addclass(index)">
       <i :class="tabber.icon"></i>
         <span>{{tabber.name}}</span>
       </li>
     </ul>
    </div>
  </div>
  </div>

</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      tabber_color:0,
      tabbers:[
       {icon:'iconfont icon-fangzi01-copy',name:'首页'},
       {icon:'iconfont icon-aixin',name:'动态'},
       {icon:'iconfont icon-03f',name:'商店'},
       {icon:'iconfont icon-wode-',name:'我的'}
      ]
    }
  },
  methods:{
    addclass(index){
      this.tabber_color=index;
    }
  }
}


</script>

<style lang="css" scoped>

@import"./../static/css/index.css";

#footer_ct{
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    height: 1.293333rem;
    background: #FBFBFB;
    z-index: 10;
}

#footer_ct ul {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-pack: distribute;
    justify-content: space-around;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    height: 1.293333rem;
    font-size: 0.02rem

}


#footer_ct  ul li {
    height: 1.093333rem;
    color: #C7C7C7;
    text-align: center;
    position: relative;
}

#footer_ct ul li i{
    display: block;
    font-size: 0.6rem;
    line-height: 0.6rem;
    text-align: center;
}


 #footer_ct ul li span {
    text-align: center;
    font-size: 0.266667rem;
    font-weight: 400;
    color: #8e8e8e;
    line-height: 0.646667rem;

}
#footer_ct ul li.active{
    color: #FE007F;
}


.iconfont {
    font-family: "iconfont" !important;
    font-size: 16px;
    font-style: normal;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}


</style>
