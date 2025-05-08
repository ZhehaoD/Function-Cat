<script setup>
import { computed } from 'vue'
import { colorsBgLight, colorsOutline } from '@/colors.js'
import CircleTagPlain from '@/components/CircleTagPlain.vue'

const props = defineProps({
  label: {
    type: String,
    required: true
  },
  color: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    default: null
  },
  large: Boolean,
  outline: Boolean
})

const componentClass = computed(() => [
  props.large ? 'py-2 px-4' : 'py-1 px-2',
  props.outline ? colorsOutline[props.color] : colorsBgLight[props.color]
])
</script>

<template>
  <CircleTagPlain
    class="border rounded-full"
    :class="componentClass"
    :icon="icon"
    :label="label"
    :large="large"
  />
</template>
