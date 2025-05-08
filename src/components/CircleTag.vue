<template>
    <button
      class="flex items-center justify-center h-8 w-8 rounded-full focus:outline-none"
      :class="['bg-' + color, { 'border-' + color: outline, 'text-' + color: outline }]"
      :disabled="disabled"
    >
      <template v-if="icon">
        <font-awesome-icon :icon="icon" />
      </template>
      <template v-else>
        <span>{{ label }}</span>
      </template>
    </button>
  </template>
  
  <script setup>
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
  import { library } from '@fortawesome/fontawesome-svg-core'
  import { faCheck } from '@fortawesome/free-solid-svg-icons'
  
  library.add(faCheck)
  
  const props = defineProps({
    color: {
      type: String,
      default: 'contrast'
    },
    label: {
      type: String,
      default: ''
    },
    outline: {
      type: Boolean,
      default: false
    },
    icon: {
      type: String,
      default: null
    },
    disabled: {
      type: Boolean,
      default: false
    }
  })
  </script>
  
  <style scoped>
  /* 可以根据需要调整样式 */
  button {
    cursor: pointer;
    transition: background-color 0.2s ease, border-color 0.2s ease, color 0.2s ease;
  }
  </style>