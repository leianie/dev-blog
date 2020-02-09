<template>
  <div>
    <section class="container mx-auto sm:px-10 pb-10 lg:w-3/4">
      <Categories />
      <article class="mx-auto lg:w-4/5">
        <Articles :articles="category.articles || []" />
      </article>
    </section> 
  </div>
</template>

<script>
import articlesQuery from '~/apollo/queries/article/articles-categories'  
import Articles from '~/components/Articles'
import Categories from '~/components/Categories'

export default {
  components: {
    Articles,
    Categories
  },
  data() {
    return {
      category: []
    }
  },
  apollo: {
    category: {
      prefetch: true,
      query: articlesQuery,
      variables () {
        return { id: parseInt(this.$route.params.id) }
      }
    }
  }
}
</script>

<style>

</style>