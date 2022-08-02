<template>
  <nav>
    <router-link to="/">About Me</router-link> | 
    <router-link to="/vue">Vue Information</router-link>
  </nav>
  <router-view/>
  <MyFooter />
</template>

<script>
import MyFooter from '@/components/MyFooter.vue'

export default {
  components: {
    MyFooter,
  }
}
</script>


<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
   max-width:500px;
   margin: 0 auto;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
