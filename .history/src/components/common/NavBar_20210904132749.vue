<template>
  <div>
     <div class="nav">

       <el-menu
          :default-active="$store.state.activeIndex"
          class="el-menu-demo"
          mode="horizontal"
          text-color="#000000"
          active-text-color="#444444"
        >
          <el-menu-item index="1" @click="itemclick">首页</el-menu-item>
          <el-menu-item index="2" @click="itemclick2">阅读</el-menu-item>
          <el-menu-item index="3" @click="itemclick3">问答</el-menu-item>
          <el-menu-item index="4" @click="itemclick4">测试</el-menu-item>
          <el-menu-item index="5" @click="itemclick5">登录/注册</el-menu-item>
        </el-menu>

     </div>

  </div>
</template>

<script>


export default {

  name: "navbar",
  data() {
    return {
    }
  },
  methods:{
    itemclick(){
      console.log('itemclick');
      this.$router.push("/")
    },
    itemclick2(){
      this.$router.push("/read")
    },
    itemclick3(){
      this.$router.push("./qs")
    },
    itemclick4(){
      this.$router.push('./test')
    },
    itemclick5(){
      this.$router.push('/login')
    }

  },

};
</script>

<style scoped>
.nav{

  margin: 0 auto;
  /* background-color: rgba(217, 221, 221, 0.918);
   */
   /* background-color: #5880A9; */
  padding: 0;


}
.nav>.el-menu{
  width: 400px;
  margin: 0 auto;
  /* background-color: rgba(217, 221, 221, 0.918); */
}

</style>

