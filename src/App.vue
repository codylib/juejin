<script setup>
import { RouterView } from 'vue-router'
import HeaderBar from '@/components/nav/index.vue'
</script>

<template>
  <div class="layout-box">
    <a-layout>
      <a-layout-header class="heade-box">
        <HeaderBar />
      </a-layout-header>
      <a-layout-content class="content-box">
        <div class="content-body">
          <RouterView />
        </div>
      </a-layout-content>
    </a-layout>
  </div>
</template>

<style scoped>
.layout-box {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row;
}

.layout-box .heade-box {
  height: 60px;
  box-shadow: 0 0 2px 0 gray;
  position: fixed;
  width: 100%;
  z-index: 999;
  background: white;
}

.layout-box .content-box {
  background-color: #f0f2f5;
  margin-top: 60px;
}

.layout-box .content-box .content-body {
  max-width: 1200px;
  margin: 0 auto;
  padding-top: 20px;
}
</style>
