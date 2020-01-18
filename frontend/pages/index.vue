<template>
  <div>
    <div class="container mx-auto">
      <header class="text-center m-16 text-4xl text-winter">
        idk_games
      </header>
      <nav class="text-center text-blue-800 mb-2">
        .
        <a href="" class="text-blue-500 visited:text-purple-500">home</a>
        .
        <a href="" class="text-blue-500 visited:text-purple-500">about</a>
        .
        <a href="" class="text-blue-500 visited:text-purple-500">contact</a>
        .
      </nav>
    </div>
    <section class="container mx-auto bg-blue-800 p-10 lg:w-2/4">
      <article>
        <div class="text-winter text-2xl">
          Sample Title
        </div>
      </article>
    </section> 
  </div>
  
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
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
