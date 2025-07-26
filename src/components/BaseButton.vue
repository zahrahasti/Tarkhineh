<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    bgButton?: string
    hasBorder?: string
    hasHeight?: 'h-[32px]' | 'h-[40px]'
    width?: string
  }>(),
  {
    bgButton: '',
    hasBorder: '',
    hasHeight: 'h-[32px]',
    width: 'w-full',
  },
)
</script>

<template>
  <button
    class="h-[32px] lg:h-[40px] w-inherite flex items-center justify-center gap-1 p-3xs rounded-sm"
    :class="[props.bgButton, props.hasHeight, props.hasBorder, props.width]"
  >
    <slot />
  </button>
</template>
