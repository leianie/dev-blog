<template>
  <div>
    <div class="container mx-auto">
      <header class="text-center m-16 text-4xl text-winter">
        idk_games
      </header>
      <nav class="text-center text-blue-800 mb-2">
        .
        <a href="" class="text-blue-500 visited:text-purple-500 hover:text-winter">home</a>
        .
        <a href="" class="text-blue-500 visited:text-purple-500 hover:text-winter">about</a>
        .
        <a href="" class="text-blue-500 visited:text-purple-500 hover:text-winter">contact</a>
        .
      </nav>
    </div>
    <nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Source Code Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
