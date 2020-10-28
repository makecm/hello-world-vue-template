<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld v-bind:msg="makeTemplateProps.headline"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

const makeTemplateMixin = {
  computed: {
    makeTemplateProps() {
      return window.templateProps || {headline: "Welcome to Your Vue.js App"};
    }
  }
}

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  mixins: [makeTemplateMixin]
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
