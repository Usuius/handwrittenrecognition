<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div id="recognition" :style="{ background: 'var(--color-fill-2)',padding:'28px'}">
    <a-layout>
        <ImageUpload/>
        <a-layout-content>
            <a-row class="content" align="center">
                <a-col>
                    <div class="startbtn">
                        <a-button type="primary" status="warning" size="large">Start!</a-button>
                    </div>
                </a-col>

            </a-row>
        </a-layout-content>
    </a-layout>
  </div>
</template>


<script setup>
import ImageUpload from './ImageUpload.vue'


</script>

<style>
.content{
    height: 500px;
    background-color: var(--color-fill-1);
}
.startbtn{
    display: flex;
    justify-content: center;
}

</style>