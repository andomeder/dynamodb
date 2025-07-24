<script setup>
import { useDark, useToggle } from '@vueuse/core'

const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
  <button
    class="bg-transparent !border-none !outline-none"
    @click="toggleDark()"
  >
    <div v-if="isDark" class="i-carbon-sun" />
    <div v-else class="i-carbon-moon" />
  </button>
</template>