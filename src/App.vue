<template>
    <div id="app">
      <AppHeader />
      <Card />
      <AppMain />
      <AppFooter />
    </div>
  </template>
  
  <script>
  import AppHeader from './components/AppHeader.vue'
  import Card from './components/Card.vue'
  import AppMain from './components/AppMain.vue'
  import AppFooter from './components/AppFooter.vue'
  
  export default {
    name: 'App',
    components: {
      AppHeader,
      Card,
      AppMain,
      AppFooter
    }
  }
  </script>
  
  <style lang="scss">
  @import '/src/components/styles/generals.scss';
  </style>
  