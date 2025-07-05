<script  setup>
import zhCn from 'element-plus/dist/locale/zh-cn.mjs'


</script>


<template>
  <el-config-provider :locale="zhCn">
    <router-view />
    <button @click="toggleLang">切换语言</button>

  </el-config-provider>
</template>