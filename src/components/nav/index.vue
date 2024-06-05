<script setup>
import router from '@/router/index.js'

const handleClick = (e) => {
  router.push(e)
}
</script>

<template>
  <a-space class="header-box">
    <div class="header-left-nav">
      <div class="header-logo"><a href="/"><img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="107" height="22" /></a></div>
      <div class="header-menu-box">
        <a-menu class="header-menu" mode="horizontal" :default-selected-keys="['/']" @menu-item-click="handleClick">
          <a-menu-item key="/">首页</a-menu-item>
          <a-menu-item key="/bots">BOT</a-menu-item>
          <a-menu-item key="/pins">沸点</a-menu-item>
          <a-menu-item key="/course">课程</a-menu-item>
          <a-menu-item key="/live">直播</a-menu-item>
          <a-menu-item key="/events">活动</a-menu-item>
          <a-menu-item key="/challenge">竞赛</a-menu-item>
          <a-menu-item key="/goods">商城</a-menu-item>
          <a-menu-item key="/app">APP</a-menu-item>
          <a-menu-item key="/extension">插件</a-menu-item>
        </a-menu>
      </div>
    </div>
    <div class="header-right-nav">
      <a-space size="large">
        <div>
          <icon-notification size="20" />
        </div>
        <div>
          <a-avatar :style="{ backgroundColor: '#3370ff' }">
            <IconUser size="16" />
          </a-avatar>
        </div>
      </a-space>
    </div>
  </a-space>
</template>

<style scoped>
.arco-icon {
  font-size: 32px;
}

.header-box {
  max-width: 1200px;
  height: 60px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

.header-left-nav {
  display: flex;
  flex-direction: row;
  height: 60px;
}

.header-logo {
  width: auto;
  height: 20px;
  margin: 20px;
}

.header-menu-box {
  flex: 1;
  width: 750px;
  height: 100%;
}

.header-menu {
  width: 100%;
  height: 100%;
}


.header-right-nav {
  margin: 24px;
}
</style>
