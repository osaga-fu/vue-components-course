<script setup>
defineProps({
  name: { type: String, default: 'Default Plan' },
  price: { type: Number, required: true },
})
</script>

<template>
  <div class="plan">
    <div class="description">
      <span class="title">{{ name }} - {{ price }} $</span>
    </div>
  </div>
</template>

<style scoped></style>
