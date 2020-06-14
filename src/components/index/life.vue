<template>
  <div class="m-life">
    <el-row>
      <ul class="nav">
        <li>
          <router-link to="/" class="takeout">吃吃喝喝</router-link>
        </li>
        <li>
          <router-link to="/" class>逛逛浪浪</router-link>
        </li>
        <li>
          <router-link to="/" class>看点电影</router-link>
        </li>
        <li>
          <router-link to="/" class="apartment">住会儿酒店</router-link>
        </li>
        <li>
          <router-link to="/" class="business">商家入驻</router-link>
        </li>
        <li>
          <router-link to="/" class>嘻嘻哈哈</router-link>
        </li>
      </ul>
    </el-row>
    <el-row>
      <el-col :span="14">
        <slider />
      </el-col>
      <el-col :span="4">
        <div class="m-life-pic"></div>
      </el-col>
      <el-col :span="6">
        <div class="m-life-login">
          <img src="http://img5.imgtn.bdimg.com/it/u=2355146281,1356141730&fm=26&gp=0.jpg" alt />
          <p class="m-life-login-name">Hi~你好</p>
          <p>
            <roter-link :to="{name: 'register'}">
              <el-button round>注册</el-button>
            </roter-link>
          </p>
          <p>
            <roter-link :to="{name: 'login'}"> <el-button round>立即登录</el-button></roter-link>
          </p>
        </div>
      </el-col>
    </el-row>
    <el-row>
        <el-col :span="7">
            <div class="m-life-hotel"></div>
        </el-col>
         <el-col :span="7">
             <div class="m-life-music"></div>
         </el-col>
          <el-col :span="4">
              <div class="m-life-coop"></div>
          </el-col>
           <el-col :span="6">
               <div class="m-life-downapp">
                   <img src="https://s1.meituan.net/bs/fe-web-meituan/60ac9a0/img/download-qr.png" alt="">
                   <p>Karry Wang</p>
                   <p class="last-p">
                       <span class="red">1元起</span>
                       吃喝玩乐
                   </p>
               </div>
           </el-col>
    </el-row>
  </div>
</template>

<script>
import slider from "./slider.vue";
export default {
  components: {
    slider
  }
};
</script>

<style lang="scss">
@import "@/assets/css/index/life.scss";
</style>