<template>
  <div id="app">
    <tab-bar>
       <tab-bar-item path="/home">
        <img slot="item-icon" src="../../../assets/img/tabbar/home.jpg" alt="">
        <img slot="item-icon-active" src="../../../assets/img/tabbar/home_active.jpg" alt="">
        <div slot="item-text">首页</div>
       </tab-bar-item>
       <tab-bar-item path="/category">
       <img slot="item-icon" src="../../../assets/img/tabbar/category.jpg" alt="">
       <img slot="item-icon-active" src="../../../assets/img/tabbar/category_active.jpg" alt="">
        <div slot="item-text">分类</div>
       </tab-bar-item>
       <tab-bar-item path="/cart">
         <img slot="item-icon" src="../../../assets/img/tabbar/shopcart.jpg" alt="">
         <img slot="item-icon-active" src="../../../assets/img/tabbar/shopcart_active.jpg" alt="">
        <div slot="item-text">购物车</div>
       </tab-bar-item>
       <tab-bar-item path="/profile">
         <img slot="item-icon" src="../../../assets/img/tabbar/profile.jpg" alt="">
         <img slot="item-icon-active" src="../../../assets/img/tabbar/profile_active.jpg" alt="">
        <div slot="item-text">我的</div>
       </tab-bar-item>
   
    </tab-bar>
    <router-view></router-view>
  </div>
</template>

<script> 
    import TabBar from '../../common/tabbar/TabBar'
    import TabBarItem from '../../common/tabbar/TabBarItem'
export default {
    name:'MainTabBar',
    components:{
        TabBar,
        TabBarItem
    }
}
</script>

<style>

</style>