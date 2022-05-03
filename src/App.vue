<script setup lang="ts">
import {ref} from "vue";

const config = ref(["","","","","","",""])

</script>

<template>

  <div class="flex justify-center items-center w-full h-30 mt-3">
    <div v-for="slot in config" >
      <img :src="`/images/${slot}.png`" class="h-32" alt="" >
    </div>
  </div>
  <div class="mx-auto w-2/5 mt-2">
    <div v-for="slot in Array.from({length: 5}, (v, i) => i) " class="w-full">

    <select class="block w-full" v-model="config[slot]">
      <option value="">choose</option>
      <option value="switch">switch</option>
      <option value="encoder">encoder</option>
      <option value="2switches">2 switches</option>
      <option value="2uswitch">2 unit switch</option>
      <option value="2stacked2uswitches">2 stackend 2 unit switches</option>
      <option value="vertical2uswitch">vertical 2 unit switch</option>
    </select>

    </div>
</div>

</template>

<style>
@import "assets/base.scss";

</style>
