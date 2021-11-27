<template>
    <div>
        <h2>{{ msg }}</h2>
        <ol>
            <li>For long expressions, use computed properties. This text has been reversed using a computed property <b>{{ computedSentence }}</b></li>
        </ol>
    </div>
</template>

<script>
export default {
    name: 'ComputedAndWatchers',
    data () {
        return {
            message: 'A sentence to perform computations on'

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