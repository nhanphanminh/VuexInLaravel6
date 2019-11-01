<template>
    <div class="container">
        <h3>this is child 2</h3>
        <h2>{{count}}</h2>
        <button @click="increaseCount()">Increase count</button>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        computed: {
            count() {
                return this.$store.state.count;
            }
        },
        methods:{
            increaseCount:function(){
                this.$store.state.count++;
            }

        }
    }
</script>
