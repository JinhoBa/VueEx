<template>
  <div>
    <PageHeader/>
    <PageMenu/>
    <PageHome/>
  </div>
  <PageFooter/>
</template>
<script>
import PageFooter from '@/components/PageFooter.vue'
import PageHeader from './components/PageHeader.vue'
import PageMenu from './components/PageMenu.vue'
import PageHome from './components/PageHome.vue'

export default {
  name: 'App',
  components: {
    PageFooter,
    PageHeader,
    PageMenu,
    PageHome
  }
}
</script>
<style>
#app {
  text-align: center;
  color: #2c3e50;
}
a{
  text-align: right;
  border-color: aliceblue;
}
</style>
