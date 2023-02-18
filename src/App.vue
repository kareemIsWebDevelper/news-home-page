<script setup>
import navBar from './components/navBar.vue'
import content from './components/content.vue'
</script>

<template>
  <header>
    <navBar />
  </header>

  <main>
      <div id="wrapper">
        <content />
      </div>
  </main>
</template>

<style scoped>
header {
  width: 350px;
  margin: auto;
  margin-top: 30px;
}

main {
  width: 350px; 
  margin: auto;
  min-height: 100vh;
}
@media screen and (min-width: 400px) {
  header{
    width: 100%;
    margin-top: 60px;
  }

  main {
    width: 100%;
    min-height: 100vh;
    margin: auto;
  }

  #wrapper {
    width: 80%;
    margin: auto;
    display: flex;
    flex-flow: column;
    gap: 20px;
  }
}
</style>
