<template>
    <!-- 悬浮气泡 -->
    <a-tooltip position="right" background-color="var(--hw-orange-)">
        <!-- 悬浮气泡内容slot -->
        <template #content>
            <p>Select two images you want to recognize here</p>
            <p>Only ".jpg" or ".png" format allowed</p>
        </template>
        <!-- 侧边图片上传栏 -->
        <a-layout-sider :width="100" :style="{background:'var(--color-bg-2)'}">
            <div :style="{margin:'10px'}">
                <!-- arco上传组件 -->
                <a-upload
                action="/"
                :custom-request="RequestUpload"
                v-model:file-list="FileList"
                :on-before-upload="OnBeforeUpload"
                :on-button-click="OnButtonClick"
                list-type="picture-card"
                accept=".jpg,.png"
                :auto-upload="false"
                image-preview
                :multiple="true"
                :limit="2">


                </a-upload>
            </div>

        </a-layout-sider>
        </a-tooltip>

</template>

<script setup>

// 上传的文件列表
//以表单方式提交两张图片
let FileList = [];
const OnBeforeUpload = (file) =>{
    console.log('OnBeforeUpload')
    console.log(file)
    console.log(FileList)
    return file
}
// 这里的button是指增加图片的button
const OnButtonClick = (Event) =>{
    console.log('OnButtonClick')
    console.log(FileList)
}

const RequestUpload = (options)=>{
    console.log("RequestUpload")
    console.log(FileList.size)
    return 
}
</script>

<style>
</style>