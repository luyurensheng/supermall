<template>
    <div>
         <swiper>
            <swiper-item v-for="(item,index) in banners" :key="index">
                <a :href="item.link">
                    <img :src="item.image" alt="">
                </a>
            </swiper-item>
        </swiper>
    </div>
</template>

<script>
// import Swiper from '../../components/common/navbar/Swiper'
// import SwiperItem from '../../components/common/navbar/SwiperItem'
    import {Swiper,SwiperItem} from '../../../components/swiper/index'
export default {
    props: {
        banners: {
            type: Array,
            default() {
                return []
            }
        }
    },
    components: {
        Swiper,
        SwiperItem
    }
}
</script>

<style scoped>

</style>