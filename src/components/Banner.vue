<template>
  <q-banner>
    <div class="row justify-between items-center">
      <div class="row">
        <div class="row items-center">
          <q-btn size="24px" id="btn" color="black" flat @click="drawerLeft = !drawerLeft" round dense icon="menu" />
          <p id="title">VASCO</p>
        </div>
        <div class="vl"></div>
        <div id="tab1">
          <img src="../assets/vascologo.png" alt="Vasco" width="24">
          <span>NOSSO CT</span>
        </div>
        <div class="vl"></div>
        <div id="tab2">
          <img src="../assets/vascologo2.png" alt="Vasco" width="24">
          <span>SÓCIO GIGANTE</span>
        </div>
      </div>
      <img id="logo" src="../assets/vasco.png" alt="Vasco">
      <div id="social" class="row">
        <a href="https://www.youtube.com/c/vasco" target="_blank"><img src="../assets/yt.png" alt="social"><q-tooltip class="bg-red-14" :offset="[10, 10]">Youtube</q-tooltip></a>
        <a href="https://twitter.com/VascodaGama" target="_blank"><img src="../assets/tw.png" alt="social"><q-tooltip class="bg-blue-4" :offset="[10, 10]">Twitter</q-tooltip></a>
        <a href="https://www.instagram.com/vascodagama/" target="_blank"><img src="../assets/insta.png" alt="social"><q-tooltip class="bg-purple" :offset="[10, 10]">Instagram</q-tooltip></a>
        <a href="https://www.facebook.com/vascodagama" target="_blank"><img src="../assets/face.png" alt="social"><q-tooltip class="bg-blue-14" :offset="[10, 10]">Facebook</q-tooltip></a>
        <a href="https://www.tiktok.com/@vasco" target="_blank"><img src="../assets/tik.png" alt="social"><q-tooltip class="bg-purple-4" :offset="[10, 10]">TikTok</q-tooltip></a>
      </div>
      <img src="../assets/tour.png" alt="Vasco" height="48">
    </div>
  </q-banner>
  <q-drawer
      behavior="mobile"
      v-model="drawerLeft"
      :width="200"
      :breakpoint="700"
      elevated
      class="bg-black text-white"
  >
      <ListDrawer/>
  </q-drawer>
  <Menu/>
</template>

<script>
import {ref} from "vue";
import ListDrawer from "@/components/ListDrawer";
import Menu from "@/components/Menu";

export default {
  name: "Banner",
  components:{
    ListDrawer,
    Menu
  },
  setup () {
    return {
      drawerLeft: ref(false)
    }
  }
}
</script>

<style scoped>
.vl {
  border-left: 2px solid #606062;
  height: 30px;
  align-self: center;
}
#title{
  font-size: 30px;
  margin-top: 20px;
  margin-right: 40px;
  font-family: "love", Helvetica, Arial, serif;
}
#tab1{
  display: flex;
  align-self: center;
  align-items: center;
  margin-left: 5px;
  margin-right: 5px;
}
#tab1 span {
  margin-left: 5px;
  font-weight: bold;
}
#tab2{
  display: flex;
  align-self: center;
  align-items: center;
  margin-left: 5px;
  margin-right: 5px;
}
#tab2 span {
  margin-left: 5px;
  font-weight: bold;
}
#social{
  margin-left: 20%;
}
#social img{
  width: 24px;
}
#logo{
  margin-left: 10%;
}
</style>