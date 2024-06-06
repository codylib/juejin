<script setup>
import {
  IconMenuFold,
  IconMenuUnfold,
  IconApps,
  IconBug,
  IconBulb
} from '@arco-design/web-vue/es/icon'
</script>

<template>
  <a-row :gutter="12">
    <a-col :span="4">
      <a-menu
        showCollapseButton
        :default-open-keys="['0']"
        :default-selected-keys="['0_1']"
        :style="{ width: `${width}px`, height: 'calc(100% - 28px)' }"
      >
        <a-sub-menu key="0">
          <template #icon>
            <IconApps></IconApps>
          </template>
          <template #title>Navigation 1</template>
          <a-menu-item key="0_0">Menu 1</a-menu-item>
          <a-menu-item key="0_1">Menu 2</a-menu-item>
          <a-menu-item key="0_2" disabled>
            Menu 3
          </a-menu-item>
        </a-sub-menu>
        <a-sub-menu key="1">
          <template #icon>
            <IconBug></IconBug>
          </template>
          <template #title>Navigation 2</template>
          <a-menu-item key="1_0">Menu 1</a-menu-item>
          <a-menu-item key="1_1">Menu 2</a-menu-item>
          <a-menu-item key="1_2">Menu 3</a-menu-item>
        </a-sub-menu>
        <a-sub-menu key="2">
          <template #icon>
            <IconBulb></IconBulb>
          </template>
          <template #title>Navigation 3</template>
          <a-menu-item key="2_0">Menu 1</a-menu-item>
          <a-menu-item key="2_1">Menu 2</a-menu-item>
          <a-menu-item key="2_2">Menu 3</a-menu-item>
        </a-sub-menu>
      </a-menu>
    </a-col>
    <a-col :span="16">
      <div class="timeline">
        <a-list>
          <a-list-item v-for="idx in 10" :key="idx" action-layout="vertical">
            <template #actions>
              <span><icon-heart />83</span>
              <span><icon-star />84</span>
              <span><icon-message />Reply</span>
            </template>
            <template #extra>
              <a-image
                height="80px"
                alt="img"
                fit="cover"
                src="https://p1-arco.byteimg.com/tos-cn-i-uwbnlip3yd/3ee5f13fb09879ecb5185e440cef6eb9.png~tplv-uwbnlip3yd-webp.webp"
              />
            </template>
            <a-list-item-meta
              title="Beijing Bytedance Technology Co., Ltd."
              description="Beijing ByteDance Technology Co., Ltd. is an enterprise located in China."
            >
            </a-list-item-meta>
          </a-list-item>
        </a-list>
      </div>
    </a-col>
    <a-col :span="4">
      <div class="signin">登录</div>
    </a-col>
  </a-row>
</template>

<style scoped>
.timeline {
  background: white;
  width: 720px;
}
</style>
