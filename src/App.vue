<template>
  <div id="app">
    <NavBar/>
    <Feed/>
    <Input/>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import Feed from './components/Feed'
import Input from './components/Input'

export default {
  name: 'App',
  components: {
    NavBar,
    Feed,
    Input,
  }
}
</script>

<style>
#app {
  width: 100%;
  height: 100%;
}
</style>
