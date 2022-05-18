
<template>
    <div :style="myStyle" v-on:click="see">B.vue</div>
</template>

<script>

export default {
    name: 'B',
    data: function () {
        return {
            myStyle: {
                backgroundColor:"red",
                width: 100 + "px"
            }
        }
    },
    methods: {
        see() {
            this.myStyle.backgroundColor = "orange"
            this.myStyle.width = parseInt(this.myStyle.width) * 1.25 + "px"
            console.log(this.myStyle)
        }
    }
}
</script>

<style scoped>

    div {
        border: 1px red dashed;
        height: 75px;
        margin: 1% auto;
        transition: width 0.5s ease-in;
    }

</style>