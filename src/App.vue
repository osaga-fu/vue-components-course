<script setup>
import AppAlert from './components/AppAlert.vue'
import FancyButton from './components/FancyButton.vue'
import GithubCard from './components/GithubCard.vue'
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

    <GithubCard username="osaga-fu" />
    <GithubCard username="danielkellyio" />

    <div class="p-5">
      <AppAlert errorType="info">New Software Update Available</AppAlert>
      <AppAlert errorType="success">Your purchased has been confirmed</AppAlert>
      <AppAlert errorType="warning">Warning: Invalid email address</AppAlert>
      <AppAlert errorType="error">Error! Task failed sucessfully</AppAlert>
    </div>
  </div>
</template>

<style scoped></style>
