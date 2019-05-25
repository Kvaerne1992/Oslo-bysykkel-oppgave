<template>
  <div id="app">
    <Bysykkel Bysykkel="Velkommen til Oslo bysykkel"/>
  </div>
</template>

<script>
import Bysykkel from './components/CardList.vue'

export default {
  name: 'app',
  components: {
    Bysykkel,
  }
}
</script>

<style scoped>
.logo{
  display: block;
  margin: 0 auto;
}

#app {
  background-color: #e6e6e6;
  margin-left: -15px;
  margin-right: -15px;
  margin-top: -15px;
}
</style>
