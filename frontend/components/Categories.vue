<template>
  <div class="pt-4 text-center mb-4">
    <span :key="category.id" v-for="category in categories">
      <router-link :to="{ name: 'categories-id', params: { id: category.id } }" class="text-blue-500 hover:text-winter active:text-black">
        {{ category.name }}
      </router-link>
    </span>
  </div>
</template>

<script>
import categoriesQuery from '~/apollo/queries/category/categories'

export default {
  data() {
    return {
      categories: [],
    }
  },
  apollo: {
    categories: {
      prefetch: true,
      query: categoriesQuery
    },
  }
}
</script>

<style>

</style>