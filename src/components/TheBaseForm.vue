<script setup lang="ts">
type BorderColorClass = 'border-error' | 'border-white' | 'border-primary' | 'border-gray-700' | 'border-gray-800' | 'border-gray-300';

type HasHeight = 'h-[32px]' | 'h-[33px]' | 'h-[40px]' | 'h-[48px]' | 'h-[56px]';
const { hasBorderClass, hasHeightClass, textColorsClass } = defineProps<{
	hasBorderClass: BorderColorClass,
	hasHeightClass: HasHeight,
	textColorsClass: string,
}>();
</script>

<template>
	<form
		@submit.prevent
		:class="[hasBorderClass]"
		class="w-input-mobile sm:w-input-sm md:w-input-md lg:w-input-lg max-w-input-desktop border-[1px] rounded-md"
	>
		<fieldset :class="[hasHeightClass,textColorsClass]" class="relative w-full flex items-center px-4">
			<slot></slot>
		</fieldset>
	</form>
</template>
