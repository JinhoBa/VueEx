<template id='app'>
  <div id ='wrapper'>
  <PageHeader/>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/fan-art">Fan-Art</router-link> |
    <router-link to="/talk">Talk</router-link> |
    <router-link to="/history">History</router-link>
  </nav>
    <PageSidebar/>
    <router-view/>
    <PageFooter/>
    </div>
</template>
<script>
// @ is an alias to /src
import PageSidebar from '@/components/PageSidebar.vue'
import PageFooter from '@/components/PageFooter.vue'
import PageHeader from '@/components/PageHeader.vue'

export default {
  name: 'HomePage',
  components: {
    PageSidebar,
    PageFooter,
    PageHeader
  }
}
</script>
<style>
*{
  text-decoration-line: none;
  color: inherit;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif
}
#app {
  text-align: center;
  color: #000000;
}

nav {
  padding: 10px;
}

nav a {
  font-weight: bold;
  color: #004D98;
}

nav a.router-link-exact-active {
  color: #A50044;
}
#wrapper{
  height: auto;
  min-height: 100%;
  padding-bottom: 50px;
}
</style>
