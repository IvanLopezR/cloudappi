<template>
  <div id="app">
    <img alt="Cloudappi logo" src="./assets/cloudappi-logo.png">
    <Users title="User List"/>
  </div>
</template>

<script>
import Users from './components/Users.vue'

export default {
  name: 'app',
  components: {
    Users
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top:10px;
  background-color: #c4f5c4;
  margin:0px;
  padding-bottom:30px;
}
</style>
