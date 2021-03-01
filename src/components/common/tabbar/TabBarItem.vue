<template>
    <div  class="tab-bar-item" @click="itemClick">
        <div v-if="!isActive"><slot name="item-icon"></slot></div>
        <div v-else><slot name="item-icon-active"></slot></div>
        
        <div :style="activeStyle">
            <slot name="item-text"></slot>
        </div>
        <!-- <slot :class="{active:isActive}" name="item-text"></slot> -->
        <!-- <img src="../../assets/img/tabbar/home.jpg" alt="">
       <div>首页</div> -->
    </div>
</template>

<script>
export default {
    name:"TabBaarItem",
    props: {
        path:String,
        activeColor:{
            type:String,
            default:'red'
        }
    },
    data() {
        return {
            // isActive:true
        }
    },
    computed: {
        isActive(){
            // 判断当前活跃的path是不是this.path
            //  /home -> item1(/home) = true
            //  /home -> item1(/category) = false
            // indexOf:如果==-1表示从$route.path没有找到this.path !==-1时表示找到了即是true
            return this.$route.path.indexOf(this.path) !== -1
        },
        activeStyle() {
            return this.isActive ? {color:this.activeColor} :{}
        }
    },
    methods: {
        itemClick() {
            this.$router.replace(this.path);
        }
    },
}
</script>

<style>
.tab-bar-item {
  /* 对多个flex均等分 */
  flex: 1;
  text-align: center;
  height: 59px;
  font-size: 14px;
}

.tab-bar-item img {
    width: 24px;
    height: 24px;
    margin-top: 3px;
    /* 去掉图片底部的像素 */
    vertical-align: middle;
    margin-bottom: 2px;

}

/* .active{
    color: red;
} */
</style>