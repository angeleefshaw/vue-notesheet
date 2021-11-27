<template>
  <div class="template-syntax">
    <h2>{{ msg }}</h2>
    <ol>
      <li>{{ bindedText }}</li>
      <li>Now we will perform a single Javascript expression within a binding --> 
        <span>{{ showText ? 'Show this if showText is true' : 'this will display if showText is false' }}</span>
      </li>
      <li v-if="directive">Directives are attributes prefixed with 
        <b>'v-'</b> and are single expressions intended to apply side affects to the DOM. This sentence as been rendered using <b>'v-if'</b>
      </li>
      <li>Directives can also take interchangable 
        <span>Arguments</span> such as <b>'v-bind:href = 'url'</b>--> 
        <a v-bind:href="url"> Check it out here!</a>
      </li>
      <li>Dynamic Arguments such as <b>'v-bind:[attributeName] = 'url'
        </b> or <b>'v-bind:[eventName]='doSomething'</b> are expected to evaluate a string. Non stringy values will trigger a warning. 
        <button v-on:[click]="handleClick">Click Me</button>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'TemplateSyntax',
  data () {
    return {
      bindedText: "This text was rendered using {{ }}",
      showText: false,
      directive: true,
      url: 'https://vuejs.org/v2/guide/syntax.html',
      click: 'click'

    }
  },
  methods: {
    handleClick () {
      alert('This alert was triggered via a Dynamic Argument!')
    }
  },
  props: {
    msg: String
  }
}
</script>


<style scoped>
h3 {
  margin: 40px 0 0;
}
li {
  padding: 6px;
}
a {
  color: #42b983;
}
span {
  font-style: italic;
}
</style>
