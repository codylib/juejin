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
        :default-open-keys="['0']"
        :default-selected-keys="['0_1']"
        :style="{ width: `${width}px`, height: 'calc(100% - 28px)' }"
      >
        <a-menu-item key="/following"><template #icon><icon-subscribe-add /></template>关注</a-menu-item>
        <a-menu-item key="/recommended"><template #icon><icon-compass /></template>综合</a-menu-item>
        <a-menu-item key="/backend"><template #icon><icon-computer /></template>后端</a-menu-item>
        <a-menu-item key="/frontend"><template #icon><icon-file-video /></template>前端</a-menu-item>
        <a-menu-item key="1_1"><template #icon><icon-apps></icon-apps></template>Android</a-menu-item>
        <a-menu-item key="1_2"><template #icon><icon-apps></icon-apps></template>IOS</a-menu-item>
        <a-menu-item key="2_0"><template #icon><icon-apps></icon-apps></template>人工智能</a-menu-item>
        <a-menu-item key="2_1"><template #icon><icon-apps></icon-apps></template>开发工具</a-menu-item>
        <a-menu-item key="2_2"><template #icon><icon-apps></icon-apps></template>代码人生</a-menu-item>
        <a-menu-item key="2_2"><template #icon><icon-apps></icon-apps></template>阅读</a-menu-item>
        <a-menu-item key="2_2"><template #icon><icon-apps></icon-apps></template>排行榜</a-menu-item>
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
.arco-icon { font-size: 18px; }
.timeline {
  background: white;
  width: 720px;
}
</style>
