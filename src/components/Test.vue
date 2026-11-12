<template>
  <v-btn @click="VeriÇek">Veri Çek</v-btn>

  {{ veri }}
</template>

<script setup lang="ts">
import axios from 'axios';
import {ref} from "vue";

var response = null;


async function VeriÇek() {
  console.log("TUŞA BASILDI");
  // response = axios.get("https://hasanadiguzel.com.tr/api/kurgetir")
  //response = await Sleep(2000);
  response = await SleepV2(2000);

  console.log(response);

  console.log("FONKSİYON BİTTİ");


}

function Sleep(ms) {

  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(`Uyku Süresi: ${ms}`)
    }, ms);
    return `ÇALIŞMIYOR BU`;
  })
}

async function SleepV2(ms) {
  var bittiMi = false;

  setTimeout(() => {
    bittiMi = true;
    console.log("Timeout içine girdi")
  }, ms)

  while (!bittiMi) {

  }
  return `Uyku Süresi: ${ms}`
}


</script>

<style scoped>

</style>