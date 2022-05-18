
<template>

    <div v-on:click="$emit('chg', $event.target.value)" :style="{backgroundColor: bgColor, width: w}">{{title}}</div>

</template>

<script>
    export default {
        name: 'A',
        props: {
            bgColor: String,
            title: String,
            w: String
        },
        emits: ['chg']
    }
</script>

<style scoped>
    div {
        border: 1px black dashed;
        height: 75px;
        margin: 1% auto;
        transition: width 0.5s ease-in;
    }
</style>