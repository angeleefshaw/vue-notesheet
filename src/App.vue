<template>
  <div id="app">
  <h1>Vue Framework Notesheet</h1>
  <span> Follow along to learn more about how the Vue framework works.</span>
  <TemplateSyntax class="m-5" msg="Template Syntax"/>
  <ComputedAndWatchers class="m-5" msg="Computed Properties and Watchers"/>
  </div>
</template>

<script>
import TemplateSyntax from './components/TemplateSyntax.vue'
import ComputedAndWatchers from './components/ComputedAndWatchers.vue'

export default {
  name: 'App',
  components: {
    TemplateSyntax,
    ComputedAndWatchers
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
