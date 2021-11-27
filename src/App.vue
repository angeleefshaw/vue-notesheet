<template>
  <div id="app">
  <h1>Vue Framework Notesheet</h1>
  <span> Follow along to learn more about how the Vue framework works.</span>
  <TemplateSyntax msg="Template Syntax"/>
  </div>
</template>

<script>
import TemplateSyntax from './components/TemplateSyntax.vue'

export default {
  name: 'App',
  components: {
    TemplateSyntax
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
