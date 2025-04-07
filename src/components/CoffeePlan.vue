<script setup>
const props = defineProps({
  name: {
    type: String,
    default: 'Default Plan',
    validator(value) {
      return value.startsWith('The')
    },
  },
  price: { type: Number, required: true },
  selected: { type: Boolean, default: false },
})

const emit = defineEmits(['selected'])

const toggleSelected = () => {
  emit('selected', props.name)
}
</script>

<template>
  <div class="plan" @click="toggleSelected" :class="{ 'active-plan': selected }">
    <div class="description">
      <span class="title">{{ name }} - {{ price }} $</span>
    </div>
  </div>
</template>

<style scoped></style>
