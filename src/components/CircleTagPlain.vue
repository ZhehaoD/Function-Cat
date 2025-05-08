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
<<<<<<< HEAD:src/components/CircleTagPlain.vue
    :class="[large ? 'w-20 h-20 text-lg' : 'w-8 h-8 text-lg']"
>>>>>>> parent of ab164d2 (Shape):src/components/CircleTagPlain.vue
=======
    :class="[Circle ? 'w-20 h-20 text-lg' : 'w-15 h-15 text-lg']"
>>>>>>> parent of fd96660 (shape):src/components/ShapeTagPlain.vue
  >
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
