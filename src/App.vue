<template>
  <a-layout style="height: 500px;">
      <a-layout-header><Header @change-tab="(key)=>tab=key"/></a-layout-header>
      <a-layout>
        <a-layout-content><Recognition/></a-layout-content>
      </a-layout>
      <!-- <a-layout-footer >Footer</a-layout-footer> -->
    </a-layout>
</template>

<script setup>
import Header from "./components/Header.vue"
import Recognition from "./components/Recognition.vue";

const tab = 0

</script>

<style>
:root{
  --hw-orange-:#fd5f00;
  --hw-white-:#f6f6e9;
  --hw-blue-:#005792;
  --hw-black-:#13334c;

}
</style>
