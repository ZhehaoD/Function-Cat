<script setup>
import BaseIcon from '@/components/BaseIcon.vue'

defineProps({
  label: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    default: null
  },
  Circle: Boolean // 添加 Circle 属性定义
})
</script>

<template>
  <div
    class="inline-flex items-center justify-center capitalize leading-none"
    :class="[Circle ? 'w-15 h-15 rounded-full' : 'w-20 h-10 rounded-lg']"
  >
    <BaseIcon
      v-if="icon"
      :path="icon"
      h="h-4"
      w="w-4"
      :class="Circle ? 'mr-2' : 'mr-1'"
    />
    <span>{{ label }}</span>
  </div>
</template>
