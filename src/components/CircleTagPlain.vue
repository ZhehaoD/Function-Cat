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
  large: Boolean,
  shadow: Boolean
})
</script>

<template>
  <div
    class="inline-flex items-center justify-center capitalize leading-none rounded-full"
    :class="[large ? 'w-20 h-20 text-lg shadow-md' : 'w-14 h-14 text-xs shadow-md', shadow ? 'shadow-md' : '']"
  >
  <div>{{ shadow }}</div>
    <BaseIcon
      v-if="icon"
      :path="icon"
      h="h-4"
      w="w-4"
      :class="large ? 'mr-2' : 'mr-1'"
      :size="large ? 20 : 16"
    />
    <span>{{ label }}</span>
  </div>
</template>
