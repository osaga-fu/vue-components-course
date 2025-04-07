<script setup>
import { ref } from 'vue'

const props = defineProps({
  username: { typeof: String, required: true },
})

fetch(`https://api.github.com/users/${props.username}`).then(async (response) => {
  const data = await response.json()
  user.value = data
})

const user = ref('')
</script>

<template>
  <div v-if="user" class="card card-side bg-base-100 shadow-sm m-5">
    <figure>
      <img
        :src="user.avatar_url"
        alt="Avatar"
      />
    </figure>
    <div class="card-body">
      <h2 class="card-title">{{user.name}}</h2>
      <p>{{user.bio}}</p>
      <div class="card-actions justify-end">
        <a class="btn btn-primary" :href="user.html_url" target="_blank">View Profile</a>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
