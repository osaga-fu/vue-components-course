<script setup>
import { ref } from 'vue'
import CoffeePlan from './CoffeePlan.vue'

const plans = ref([
  { name: 'The Hacker', price: 10 },
  { name: 'The Single', price: 8 },
  { name: 'The Double', price: 15 },
])

const selectedCoffeePlan = ref('')

const handleSelectCoffeePlan = (name) => {
  selectedCoffeePlan.value = name
}
</script>

<template>
  <div class="plans">
    {{ selectedCoffeePlan }}
    <CoffeePlan
      v-for="plan in plans"
      :key="plan"
      :name="plan.name"
      :price="plan.price"
      :selected="plan.name === selectedCoffeePlan"
      @selected="handleSelectCoffeePlan"
    />
  </div>
</template>

<style scoped></style>
