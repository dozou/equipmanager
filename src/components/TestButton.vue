<template>
    <div>
        <h1>Sand Box</h1>
        <button v-on:click="next()">Next</button>
        <button v-on:click="prev()">Prev</button>
        <button v-on:click="show()">Console show</button>
        <p>{{count}}</p>
    </div>
</template>

<script>
    export default {
        name: "TestButton",
        data(){
            return {
                count: 0
            }
        },
        methods: {
            show() {
                console.log(this.count)
            },
            next(){
                this.count++
            },
            prev(){
                this.count--
            }
        }
    }
</script>

<style scoped>

</style>