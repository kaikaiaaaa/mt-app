<template>
<div class="slide">
    <el-carousel>
      <el-carousel-item v-for="item in imgList" :key="item.img">
        <img :src="item.img" alt="">
      </el-carousel-item>
    </el-carousel>
</div>
</template>
<script>
// import slider from './slider.vue'
export default {
    data(){
        return{
            imgList:[{
                url:'#xxx',
                img:'http://img1.imgtn.bdimg.com/it/u=3592137449,1062668934&fm=26&gp=0.jpg'

            },{
                url:'#xxx',
                img:'http://t7.baidu.com/it/u=1138520732,2060293950&fm=193'
            },
            {
                 url:'#xxx',
                img:'http://img0.imgtn.bdimg.com/it/u=2385446451,3924115729&fm=26&gp=0.jpg'

            }]
        }
    }
}
</script>

<style>

</style>