<template>
  <van-grid-item>
    <template #icon>
      <app-icon :icon="icon" :size="24" />
    </template>
    <template #text>
      <div class="display-flex flex-column align-items-center">
        <div class="font-400 text-size-12 text-center text-muted">{{ title }}</div>
        <div :class="subtitleClass">{{ subtitle }}</div>
      </div>
    </template>
  </van-grid-item>
</template>
<script setup>
const props = defineProps({
  title: {},
  subtitle: {},
  subtitleClass: {},
  icon: {},
})

const subtitleClass = computed(() => {
  return `font-700 text-size-12 text-center ${props.subtitleClass}`
})
</script>
