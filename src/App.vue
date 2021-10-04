<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Here are the list of all users</h1>
  <HelloWorld />
  <CreateUser />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CreateUser from './components/CreateUser.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    CreateUser
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
