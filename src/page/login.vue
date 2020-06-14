<template>
  <div class="page-login">
      <div class="login-header">
          <a class="logo" href="http:''www.meituan.com"></a>
      </div>
      <div class="login-panel">
          <div class="banner">
              <img src="https://dss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=372152402,3249200991&fm=111&gp=0.jpg" width='480' height = '370' alt="Wangjunkai">
          </div>
          <div class="form">
              <h4 v-if="error" class="tips">{{error}}</h4>
              <p>
                  <span>账号登录</span>
              </p>
              <el-input :class="{error: error && !userName}" v-model="userName" placeholder="用户名/手机号" prefix-icon="profile"></el-input>
              <el-input :class="{error: error && !password}" type="password" v-model="password" placeholder="密码" prefix-icon="password"></el-input>
              <div class="foot">
                 <a href="#">忘记密码</a> 
              </div>
               <el-button class="btn-login" type="success" @click="submit">登录</el-button>
               <p class="reg">
                   <span>还有没有账号？</span>
                   <router-link :to="{name:'register'}">免费注册</router-link>
               </p>
               <div class="oauth-wrapper">
                   <h3 class="title-wrapper"><span class="title">用户合作网站号登录</span></h3>
                   <div class="pauth cf">
                       <a href=""></a>
                       <a href=""></a>
                   </div>
               </div>
          </div>
      </div>
    <footer>
        <ul>
            <li><a href="#">关于</a></li>
            <li><a href="#">加入我们</a></li>
            <li><a href="#">商家中心</a></li>
            <li><a href="#">帮助中心</a></li>
            <li><a href="#">手机版</a></li>
        </ul>
        <p>
            .............xxx
        </p>
    </footer>
  </div>
</template>

<script>
import api from '@/api/index.js'
export default {
    data(){
        return{
            userName:'',
            password:'',
            error:'',
        }
    },
    methods:{
        submit(){
            // console.log(this.userName,this.password)
            if(!this.userName){
                this.error = "请输入账号"
                return false;

            }
            if(!this.password){
                 this.error = "请输入密码"
                return false;

            }
            api.login({
                params:{
                    userName:this.userName,
                    password:this.password
                }
            }).then((res) => {
                console.log(res)
                if(res.data.status == 'success'){
                    this.$router.push({name:'index'})
                }else{
                    this.error = res.data.msg;
                }
            })
        }
    }
}
</script>

<style lang = "scss">
@import "@/assets/css/login/index.scss"

</style>