<template>
    <div class="recommend">
        <!-- v-for要绑定key才不会报错 -->
        <div v-for="item in recommends">
            <a :href="item.link">
                <img :src="item.image" alt="">
                <div>{{item.title}}</div>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        recommends: {
            type:Array,
            default() {
                return []
            }
        }
    }
}
</script>

<style scoped>
.recommend {
    display: flex;
    width: 100%;
    text-align: center;
    font-size: 12px;
    padding: 10px 0 20px;
    border-bottom: 10px solid #eee;
}
.recommend-item {
    flex: 1;
}
.recommend img {
    width: 100%;
    margin-bottom: 10px;
}

</style>