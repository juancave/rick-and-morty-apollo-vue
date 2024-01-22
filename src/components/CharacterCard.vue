<script setup lang="ts">
import type { Character } from '../interfaces/Character'

defineProps<Character>()
</script>

<template>
  <article class="card">
    <div class="image-wrapper">
      <img :src="image" :alt="name">
    </div>
    <div class="content">
      <div class="section">
        <h2 class="green">{{ name }}</h2>
      </div>
      <hr>
      <div class="section">
        <span class="bold">Status: </span><span>{{ status }}</span>
      </div>
      <div class="section">
        <span class="bold">Species: </span><span>{{ species }}</span>
      </div>
      <div class="section">
        <span class="bold">Gender: </span><span>{{ gender }}</span>
      </div>
    </div>
  </article>
</template>

<style scoped>
h2 {
  font-weight: bold;
}
</style>
