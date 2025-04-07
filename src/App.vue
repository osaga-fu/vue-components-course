<script setup>
import FancyButton from './components/FancyButton.vue'
import GithubCard from './components/GithubCard.vue';
import PlanPicker from './components/PlanPicker.vue'
</script>

<template>
  <div class="content">
    <h1 class="title">Coffee Plans</h1>

    <h2 class="subtitle">
      We travel the world to source the very best single origin coffee for you
    </h2>

    <PlanPicker />

    <FancyButton>
      <template #icon="{ hover }">
        {{ hover ? '👋' : '💪' }}
      </template>
      Submit
    </FancyButton>

    <GithubCard username="osaga-fu"/>
    <GithubCard username="danielkellyio"/>
  </div>
</template>

<style scoped></style>
