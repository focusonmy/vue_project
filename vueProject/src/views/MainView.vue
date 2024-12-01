<template>
  <Header :mensaje="texto"/>
  <div class="container">
    <Sidebar />
    <div class="content">
      <input type="text" v-model="texto"/>
      {{ texto }}
      <router-view />
    </div>
  </div>
</template>

<script setup>
import Sidebar from "../components/SideBar.vue";
import Header from "../components/Header.vue";
import { ref } from "vue";

const texto = ref('');
</script>

<style scoped>
.container {
  margin-top: 40px;
  display: flex;
}
.content {
  margin-top: 20px;
  flex: 1;
  padding: 20px;
}
</style>
