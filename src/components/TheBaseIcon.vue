<script lang="ts" setup>
const props = defineProps<{
  color?: {
    type: string
    default: '#FFF'
  }
  name: string
}>()
</script>

<template>
  <div class="w-4 sm:w-6">
    <VsxIcon :icon-name="props.name" :size="undefined" :color="props.color" type="linear" />
  </div>
</template>
