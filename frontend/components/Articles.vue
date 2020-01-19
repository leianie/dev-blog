<template>
  <div>
    <div :key="article.id" v-for="article in articles">
      <div class="text-winter text-2xl text-center">
        {{ article.title }}
      </div>
      <div class="mx-auto w-128">
        <img :src="url + article.image.url" />
      </div>
    </div>
  </div>
</template>

<script>
import articlesQuery from '~/apollo/queries/article/articles'

export default {
  props: {
    articles: Array
  },
  data() {
    return {
      url: process.env.url
    }
  }
}
</script>

<style>
  .w-128 {
    width: 32rem;
  }
</style>