<template>
<div>
  <img class="logo" src="../assets/logo.png">
  <div class="box">
    <div class="show-pic">
    </div>
    <div class="login-wrapper">
      <div class="user-wrapper">
        <img src="../assets/user.svg" class="user">
        <input type="text" placeholder="请输入账号">

      </div>
      <div class="key-wrapper">
        <img src="../assets/key.svg" class="key">
        <input type="text" placeholder="请输入密码">

      </div>
      <div class="btn" @click="goToHome()">
        登陆
      </div>
      <div class="link" @click="goToRegister()">没有账号？立即注册</div>

    </div>

  </div> 

</div>

   
</template>

<script>
export default {
  name: "",
  methods: {
    goToHome(){
      this.$router.push({
        path: "/"
      });
    },
    goToRegister() {
      this.$router.push({
        path: "/register"
      });
    }
  }
};
</script>

<style scoped>
.logo {
  position: absolute;
  width: 350px;
  height: 141px;
  left: 50px;
  top: 50px;
}

.box {
  position: relative;
  height: 560px;
  width: 100%;
  background-color: rgba(229, 229, 229, 0.5);
  top: 250px;
  align-items: center;
  display: flex;
  justify-content: space-around;
}

.show-pic {
  position: relative;
  height: 400px;
  width: 45vw;
  margin-left: 80px;
  /* margin-top: -50px; */
  background-image: url("../assets/turn1.jpg");
  border-radius: 150px;
  overflow: hidden;
  background-size: 100%;
  display: inline;
}

.login-wrapper {
  display: inlie;
  height: 450px;
  width: 30vw;
  background-color: rgba(255, 255, 255, 1);
  border-radius: 16px;
  margin-right: 110px;
  justify-content: center;
  align-content: center;
  
}

.user-wrapper{
  margin-top: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}

input{
  display: inline-block;
  height: 45px;
  width: 16vw;
  background-color:rgba(229, 229, 229, 0.5);
  font-size: 20px;
  color: rgba(51, 51, 51, 1);
  margin-left: 5px;

}
.user {
  display: inline-block;
  height: 45px;
  width: 45px;
}

.key-wrapper{
   display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 40px;

}

.key {
  display: inline-block;
  height: 45px;
  width: 45px;
}

.btn{
  margin-top: 40px;
  height: 50px;
  width: 8vw;
  background-color: rgba(255, 195, 0, 1);
  border-radius: 18px;
  font-size: 24px;
  font-weight: bold;
  line-height: 50px;
  text-align: center;
  margin-left: auto;
  margin-right: auto;

}

.btn:hover{
  background-color: black;
  color: white;
  transition-duration: 0.8s;
  cursor: pointer;

}

.link{
  margin-top: 20px;
  font-size: 16px;
  color: rgba(255, 141, 26, 1);
  text-decoration:underline;
}
.link:hover{
  cursor: pointer;
}
</style>