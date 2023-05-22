<template>
  <PageHeader/>
  <div class="container">
    <PageMenu/>
    <router-view/>
  </div>
  <PageFooter/>
</template>
<script>
import PageFooter from '@/components/PageFooter.vue'
import PageHeader from '@/components/PageHeader.vue'
import PageMenu from '@/components/PageMenu.vue'

export default {
  name: 'App',
  components: {
    PageHeader,
    PageFooter,
    PageMenu
  }
}
</script>
<style>
  .container{
    display: flex;
  }
  aside{
    width: 20%;
    background-color: cornflowerblue;
  }
  #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
