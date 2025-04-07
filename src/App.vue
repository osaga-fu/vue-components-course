<script setup>
import CoffeePlan from './components/CoffeePlan.vue';


</script>

<template>
  <div class="content">
    <h1 class="title">Coffee Plans</h1>

    <h2 class="subtitle">
      We travel the world to source the very best single origin coffee for you
    </h2>

    <div class="plans">
      <CoffeePlan name="The Hacker" />
      <CoffeePlan name="The Single" />
      <CoffeePlan name="The Double" />
    </div>
  </div>
</template>

<style scoped></style>
