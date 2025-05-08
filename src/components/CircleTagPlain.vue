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
    class="inline-flex items-center capitalize leading-none"
    :class="[large ? 'text-sm' : 'text-xs']"
  >
    <BaseIcon
      v-if="icon"
      :path="icon"
      h="h-4"
      w="w-4"
      :class="large ? 'mr-1' : 'mr-2'"
      :size="large ? null : 14"
    />
    <span>{{ label }}</span>
  </div>
</template>
