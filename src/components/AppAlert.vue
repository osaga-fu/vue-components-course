<script setup>
import { computed, ref } from 'vue'
import IconInfo from './icons/IconInfo.vue'
import IconWarning from './icons/IconWarning.vue'
import IconSuccess from './icons/IconSuccess.vue'
import IconError from './icons/IconError.vue'

const props = defineProps({
  errorType: { typeof: String, default: 'info' },
})

const icon = computed(() => {
  return {
    info: IconInfo,
    warning: IconWarning,
    success: IconSuccess,
    error: IconError,
  }[props.errorType]
})

const closed = ref(false)

const handleClose = () => {
  closed.value = true
  console.log('Close alert ' + props.errorType)
}
</script>

<template>
  <div v-if="!closed" role="alert" class="alert" :class="`alert-${errorType}`">
    <component :is="icon"></component>
    <span><slot></slot></span>
    <span @click="handleClose" class="close-alert">X</span>
  </div>
</template>

<style scoped>
.close-alert:hover {
  cursor: pointer;
}
</style>
