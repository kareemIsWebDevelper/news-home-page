<script>

export default {
  data: function (){
    return {
      isVisible: false
    }
  },
  methods: {
    toggle(){
      this.isVisible = !this.isVisible
    }
  },
  computed: {
    
  }
}
</script>

<template>
  <div id="nav-bar">
    <div id="logo">
      <img src="../assets/images/logo.svg" alt="logo">
    </div>
    <div class="dropdown">
      <img src="../assets/images/icon-menu.svg" v-on:click="toggle" class="dropMenu">
      <div v-if="isVisible" class="dropdown-content">
      <a href="#">Home</a>
      <a href="#">New</a>
      <a href="#">Popular</a>
      <a href="#">Trending</a>
      <a href="#">Categories</a>
      </div>
    </div>
    <div class="links">
      <a href="#">Home</a>
      <a href="#">New</a>
      <a href="#">Popular</a>
      <a href="#">Trending</a>
      <a href="#">Categories</a>
      </div>
  </div>
</template>

<style scoped>
  .links {
    display: none;
  }

  @media screen and (min-width: 400px) {
    .dropdown {
      display: none;
    }
    .links {
      display: inline-block;
    }
    .links a {
      text-decoration: none;
      padding-right: 30px;
      color: black;
      font-size: 15px;
    }
    .links a:hover {
      color: red;
    }

    #nav-bar {
      width: 80%;
      display: flex;
      justify-content: space-between;
      margin: auto;
    }
  }
</style>
