<script setup lang="ts">
defineProps<{
  id: string
  name: string
  status: string
  species: string
  gender: string
}>()
</script>

<template>
  <article class="card">
    <div class="image-wrapper">
      <img :src="'https://rickandmortyapi.com/api/character/avatar/' + id + '.jpeg'" :alt="name">
    </div>
    <div class="content">
      <div class="section">
        <h2 class="green">{{ name }}</h2>
      </div>
      <hr>
      <div class="section">
        <span class="bold">Status: </span><span class="status"><span class="status-icon"></span>{{ status }} {{ species }}</span>
      </div>
      <div class="section">
        <span class="bold">Gender: </span><span class="gender">{{ gender }}</span>
      </div>
    </div>
  </article>
</template>

<style scoped>
h2 {
  font-weight: bold;
}
</style>
