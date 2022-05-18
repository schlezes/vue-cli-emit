<template>
    <A bgColor="lime" title="A.vue" w="100px" v-on:chg="log"/>
    <B />
</template>

<script>
import A from './components/A.vue'
import B from './components/B.vue'

export default {
    name: 'App',
    components: {
        A,
        B

    },
    methods: {
        log() {
            console.log(event.target)
            console.log(event.target.nextSibling)
            console.log(event.target.nextSibling.style.backgroundColor)
            event.target.nextSibling.style.backgroundColor = event.target.style.backgroundColor
            console.log(event.target.style)
            console.log(event.target.style.backgroundColor)
            console.log(event.target.clientHeight)
            console.log(event.target.clientWidth)
            console.log(event.target.style.width)
            event.target.style.width = parseInt(event.target.style.width) * 1.25 + "px"
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
    }
</style>
