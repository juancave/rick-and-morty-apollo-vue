<script setup lang="ts">
import CharacterCard from '../components/CharacterCard.vue'

import gql from 'graphql-tag'
import { useQuery } from '@vue/apollo-composable'

const CHARACTERS_QUERY = gql`
  query Characters {
    characters {
      results {
        id
        name
        status
        image
        species
        gender
      }
    }
  }
`

const { result, loading, error } = useQuery(CHARACTERS_QUERY)

</script>

<template>
  <div class="container">
    <p v-if="error">Something went wrong...</p>
    <p v-if="loading">Loading...</p>
    <template v-else v-for="character in result.characters.results" :key="character.id">
      <CharacterCard v-bind="character" />
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