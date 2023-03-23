<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <!-- 首部 -->
  <div id="header">
    <!-- 页头 -->
    <div :style="{ background: 'var(--color-fill-2)',padding:'28px 28px 0px 28px' }" >
    
    <a-page-header
      :style="{ background: 'var(--color-bg-2)' }"
      title="Hand Writting Recognition Syestem"
      subtitle="Based on Deep Learning"
      :show-back="false"
    >
    
      <template #extra>
        <a-popover position="bottom">
        <a-avatar :style="{ backgroundColor: 'var(--hw-orange-)' }">
        <IconUser />
        </a-avatar>
        <template #content>
            <p>{{ username }}</p>
            <p>退出登录</p>
            <p>查看上传记录</p>
        </template>
    </a-popover>
      </template>
    </a-page-header>
  </div>
  <!-- 菜单 -->
  <div :style="{background: 'var(--color-fill-2)',padding:'0px 28px 0px 28px' }">
    <a-menu 
    mode="horizontal" 
    :default-selected-keys="['2']" 
    @menu-item-click="selectTab"
    :style="{background: 'var(--color-bg-2)'}">
      <a-menu-item key="1">Home</a-menu-item>
      <a-menu-item key="2">Recognition</a-menu-item>
      <a-menu-item key="3">Upload</a-menu-item>
      <a-menu-item key="4">Contact Us</a-menu-item>
    </a-menu>
  </div>
  </div>
</template>

<script setup>

import {IconUser} from "@arco-design/web-vue/es/icon"
import { defineEmits } from "vue";

const username = "Unknown"
const emit= defineEmits(['change-tab'])

function selectTab(key){
    // console.log(key)
    // console.log(typeof key)
    emit('change-tab',key)
}

</script>

<style>

</style>