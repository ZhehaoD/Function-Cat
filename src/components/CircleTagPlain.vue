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
  large: Boolean
})
</script>

<template>
  <div
    class="inline-flex items-center justify-center capitalize leading-none rounded-full"
    :class="[large ? 'w-16 h-16 text-lg' : 'w-15 h-15 text-xs', 'bg-gray-200']"
  >
    <BaseIcon
      v-if="icon"
      :path="icon"
      h="h-6"
      w="w-6"
      :class="large ? 'mr-2' : 'mr-1'"
      :size="large ? 20 : 14"
    />
    <span>{{ label }}</span>
  </div>
</template>
