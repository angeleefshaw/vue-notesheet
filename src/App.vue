<template>
  <div id="app">
  <h1>Vue Framework Notesheet</h1>
  <span> Follow along to learn more about how the Vue framework works.</span>
  <TemplateSyntax class="m-5" msg="Template Syntax"/>
  <button v-on:click="increment">Review Complete</button>
  <ComputedAndWatchers class="m-5" msg="Computed Properties and Watchers"/>
  <button v-on:click="increment">Review Complete</button>
  </div>
</template>

<script>
import TemplateSyntax from './components/TemplateSyntax.vue'
import ComputedAndWatchers from './components/ComputedAndWatchers.vue'
import count from './store/Count'

export default {
  name: 'App',
  components: {
    TemplateSyntax,
    ComputedAndWatchers
  },
  store: count,
  methods: {
  increment() {
    this.$store.commit('increment')
    console.log(this.$store.state.count)
  }
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
