<template>
  <v-app-bar>
    <template #prepend>
      <v-app-bar-nav-icon class="d-md-none" @click="navDrawer=!navDrawer">

      </v-app-bar-nav-icon>
    </template>

    <v-app-bar-title>KURTLAR SOFRASI 2</v-app-bar-title>


    <v-btn>Oynanış</v-btn>
    <v-btn @click="Login">
      <template #prepend>
        <v-icon>mdi-login</v-icon>
      </template>
      <template #default>
        Login
      </template>
    </v-btn>

  </v-app-bar>


  <v-navigation-drawer v-model="navDrawer">
    <v-container class="d-flex bg-black fill-height flex-column" fluid>
      <p class="text-center">KURTLAR SOFRASI</p>

      <v-btn class=" mb-4">Oynanış</v-btn>
      <v-btn color="green" class="mb-4">Login</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="red">Logout</v-btn>


    </v-container>
  </v-navigation-drawer>

</template>

<script setup lang="ts">
import {ref} from "vue";

var navDrawer = ref(false);

var girişYazısı = ref("Login");

function Login() {
  console.log("Tuş çalıştı")
  if (girişYazısı.value === 'Login') {
    console.log("Değer==LOGIN")
    girişYazısı.value = 'Logout';
  } else {
    console.log("Değer==LOGIN DEGIL")
    girişYazısı.value = 'Login';
  }
}

</script>


<style scoped>

</style>