<template>
    <div>
        <h2>{{ msg }}</h2>
        <ol>
            <li>For long expressions, use computed properties. This text has been reversed using a computed property <b>{{ computedSentence }}</b></li>
        </ol>
        <p>So what is the difference between computed <span>properties, watchers, and methods</span>?</p>
        <ul v-for="item in vueExpressions" :key="item.name">
            <li>{{ item['name'] }} : {{ item['description']}}</li>
        </ul>
        <a :href="href">Learn More</a>
    </div>
</template>

<script>
export default {
    name: 'ComputedAndWatchers',
    data () {
        return {
            message: 'A sentence to perform computations on',
            href:'https://flaviocopes.com/vue-methods-watchers-computed-properties/',
            vueExpressions: [
                {
                name: 'Computed Property',
                description: 'Reactive with caching based on reactive dependencies. Computed properties will only re-evaluate when reactive dependencies change.'
                },
                {
                name: 'Methods',
                description: 'to be filled in'
                },
                {
                name: 'Watchers',
                description: 'Used to perform asynchronous or expensive operations in response to changing data'
                }
            ]

        }
    },
    props: {
        msg: String
    },
    computed: {
        computedSentence() {
            return this.message.split('').reverse('').join('');
        }
    }
}
</script>

<style scoped>
a {
  color: #42b983;
}
span {
  font-style: italic;
}
</style>