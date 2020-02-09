<template>
  <div>
    <div :key="article.id" v-for="article in articles" class="bg-blue-900 mb-4 p-4">
      <div class="text-winter text-3xl text-center mb-4">
        {{ article.title }}
      </div>
      <div class="mx-auto lg:w-4/5">
        <img class="mx-auto" :src="url + article.image.url" />
      </div>
      <div class="mx-auto lg:w-4/5 text-winter text-xs sm:text-base mt-4">
        <span v-html="$md.render(toParagraph(article.content))"></span>
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
  },
  mounted() {
    // console.log(JSON.stringify(this.articles[0].content))
  },
  methods: {
    toParagraph(content) {
      return JSON.parse(JSON.stringify(content).replace(/\\n/g, '<br>'))
    }
  }
}
</script>

<style>
</style>