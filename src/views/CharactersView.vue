<script setup lang="ts">
import CharacterCard from '../components/CharacterCard.vue'

const mockData = [
  {
    "id": "1",
    "name": "Rick Sanchez",
    "status": "Alive",
    "species": "Human",
    "gender": "Male"
  },
  {
    "id": "2",
    "name": "Morty Smith",
    "status": "Alive",
    "species": "Human",
    "gender": "Male"
  },
  {
    "id": "3",
    "name": "Summer Smith",
    "status": "Alive",
    "species": "Human",
    "gender": "Female"
  },
  {
    "id": "4",
    "name": "Beth Smith",
    "status": "Alive",
    "species": "Human",
    "gender": "Female"
  },
  {
    "id": "5",
    "name": "Jerry Smith",
    "status": "Alive",
    "species": "Human",
    "gender": "Male"
  },
  {
    "id": "6",
    "name": "Abadango Cluster Princess",
    "status": "Alive",
    "species": "Alien",
    "gender": "Female"
  },
  {
    "id": "7",
    "name": "Abradolf Lincler",
    "status": "unknown",
    "species": "Human",
    "gender": "Male"
  },
  {
    "id": "8",
    "name": "Adjudicator Rick",
    "status": "Dead",
    "species": "Human",
    "gender": "Male"
  }
];

</script>

<template>
  <div class="container">
    <template v-for="item in mockData">
      <CharacterCard
        :name="item.name" :gender="item.gender" :id="item.id" :status="item.status" :species="item.species" />
    </template>
  </div>
</template>

<style scoped>
  .container {
    display: flex;
    justify-content: center;
    gap: 2rem;
    flex-wrap: wrap;
  }
</style>