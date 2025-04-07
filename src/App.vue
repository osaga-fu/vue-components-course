<script setup>
import { ref } from 'vue'
import CoffeePlan from './components/CoffeePlan.vue'

const plans = ref([
  { name: 'The Hacker', price: 10 },
  { name: 'The Single', price: 8 },
  { name: 'The Double', price: 15 },
])
</script>

<template>
  <div class="content">
    <h1 class="title">Coffee Plans</h1>

    <h2 class="subtitle">
      We travel the world to source the very best single origin coffee for you
    </h2>

    <div class="plans">
      <CoffeePlan v-for="plan in plans" :key="plan" :name="plan.name" :price="plan.price" />
    </div>
  </div>
</template>

<style scoped></style>
