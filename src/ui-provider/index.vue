<script setup lang="ts">
import { Locale } from '@nutui/nutui'
import zhCN from '@nutui/nutui/dist/packages/locale/lang/zh-CN'
import useSettingsStore from '@/store/modules/settings'

const settingsStore = useSettingsStore()

Locale.use('zh-CN', zhCN)
</script>

<template>
  <NutConfigProvider :theme="settingsStore.currentColorScheme" class="min-h-vh supports-[(min-height:100dvh)]:min-h-dvh">
    <slot />
  </NutConfigProvider>
</template>
