<script setup>
</script>

<template>
  <a-row :gutter="20">
    <a-col :span="4">
      <div class="sider-menu">
        <a-menu
          :default-selected-keys="['/recommended']"
          :style="{ width: `100%`, height: 'calc(100% - 28px)' }"
        >
          <a-menu-item key="/following">
            <template #icon>
              <icon-subscribe-add />
            </template>
            关注
          </a-menu-item>
          <a-menu-item key="/recommended">
            <template #icon>
              <icon-compass />
            </template>
            综合
          </a-menu-item>
          <a-menu-item key="/backend">
            <template #icon>
              <icon-computer />
            </template>
            后端
          </a-menu-item>
          <a-menu-item key="/frontend">
            <template #icon>
              <icon-file-video />
            </template>
            前端
          </a-menu-item>
          <a-menu-item key="/android">
            <template #icon>
              <icon-robot />
            </template>
            Android
          </a-menu-item>
          <a-menu-item key="/ios">
            <template #icon>
              <icon-apps></icon-apps>
            </template>
            IOS
          </a-menu-item>
          <a-menu-item key="/ai">
            <template #icon>
              <icon-apps></icon-apps>
            </template>
            人工智能
          </a-menu-item>
          <a-menu-item key="/freebie">
            <template #icon>
              <icon-apps></icon-apps>
            </template>
            开发工具
          </a-menu-item>
          <a-menu-item key="/career">
            <template #icon>
              <icon-apps></icon-apps>
            </template>
            代码人生
          </a-menu-item>
          <a-menu-item key="/article">
            <template #icon>
              <icon-apps></icon-apps>
            </template>
            阅读
          </a-menu-item>
          <a-menu-item key="/hot">
            <template #icon>
              <icon-apps></icon-apps>
            </template>
            排行榜
          </a-menu-item>
        </a-menu>
      </div>
    </a-col>
    <a-col :span="14">
      <div class="timeline">
        <a-list>
          <a-list-item v-for="idx in 20" :key="idx" action-layout="vertical">
            <template #actions>
              <span><icon-eye />83k</span>
              <span><icon-thumb-up />84</span>
              <span><icon-reply />分享</span>
            </template>
            <template #extra>
              <a-image
                width="120px"
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
    <a-col :span="6">
      <a-space direction="vertical" class="signin" style="display: flex; flex-direction: column">
        <div class="signin-content">
          <div>
            <div style="font-size: 16px">上午好！</div>
            <div style="font-size: 12px; color: gray; margin-top: 2px">点亮在社区的每一天</div>
          </div>
          <a-button type="outline" size="large">去签到</a-button>
        </div>
        <a-card title="文章榜">
          <template #extra>
            <icon-refresh />换一换
          </template>
          ByteDance's core product, Toutiao ("Headlines"), is a content platform in
          China and around the world. Toutiao started out as a news recommendation
          engine and gradually evolved into a platform delivering content in various
          formats.
        </a-card>
      </a-space>
    </a-col>
  </a-row>
</template>

<style scoped>
.sider-menu .arco-icon {
  font-size: 20px;
}

.timeline {
  background: white;
  width: 100%;
}

.signin {
  width: 100%;
}

.signin-content {
  background: white;
  padding: 20px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
