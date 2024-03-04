<template>
  <view class="demo">
    <view>
      欢迎使用 NutUI 开发 Taro 多端项目 <Dongdong />
    </view>
    <view>{{ count }}</view>
    <view>
      <nut-button type="primary" @click="handleClick">
        Count++
      </nut-button>
    </view>
  </view>
</template>

<script setup>
import { ref } from 'vue';
import { Dongdong } from '@nutui/icons-vue-taro';
import Taro from '@tarojs/taro'

const count = ref(0);

const handleClick = () => {
  Taro.navigateTo({
    url: 'pages/test/index'
  })
};
</script>

<style>
.demo {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>