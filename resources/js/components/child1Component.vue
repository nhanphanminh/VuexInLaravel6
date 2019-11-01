<template>
    <div class="container">
        <h3>this is child 1</h3>
        <h2>{{count}}</h2>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        computed: {
            count() {
                return this.$store.state.count
            }
        }
    }
</script>
