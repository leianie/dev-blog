<template>
  <div>
    <section class="container mx-auto bg-blue-800 px-10 pb-10 lg:w-3/4">
      <div class="pt-4">
        <span :key="category.id" v-for="category in categories">
          <router-link :to="{ name: 'categories-id', params: { id: category.id } }" class="hover:text-blue-500 active:text-blue-500">
            {{ category.name }}
          </router-link>.
        </span>
      </div>
      <article class="mx-auto lg:w-4/5">
        <Articles :articles="articles" />
      </article>
    </section> 
  </div>
  
</template>

<script>
import categoriesQuery from '~/apollo/queries/category/categories'
import articlesQuery from '~/apollo/queries/article/articles'
import Articles from '~/components/Articles'

export default {
  components: {
    Articles
  },
  data() {
    return {
      categories: [],
      articles: []
    }
  },
  apollo: {
    categories: {
      prefetch: true,
      query: categoriesQuery
    },
    articles: {
      prefetch: true,
      query: articlesQuery,
      variables() {
        return { id: parseInt(this.$route.params.id) }
      }
    }
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/

body {
  background-color: theme('colors.black');
}
</style>
