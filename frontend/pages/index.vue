<template>
  <div>
    <section class="container mx-auto sm:px-10 pb-10 lg:w-3/4">
      <Categories />
      <article class="mx-auto lg:w-4/5">
        <Articles :articles="articles" />
      </article>
    </section> 
  </div>
</template>

<script>
import articlesQuery from '~/apollo/queries/article/articles'
import Articles from '~/components/Articles'
import Categories from '~/components/Categories'

export default {
  components: {
    Articles,
    Categories
  },
  data() {
    return {
      articles: []
    }
  },
  apollo: {
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
