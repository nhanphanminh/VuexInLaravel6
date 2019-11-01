<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">This is parrents Component</div>
                    <h2>{{count}}</h2>
                    <br/>
                    <hr/>
                    <div class="card-body">
                        <child1></child1>
                        <br/>
                        <hr/>
                        <child2></child2>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Child1Component from './child1Component';
    import Child2Component from './child2Component';
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        components: {
            'child1': Child1Component,
            'child2': Child2Component
        },
        computed: {
            count() {
                //store.state.count = store.state.count + 1
                return this.$store.state.count
            }
        }
    }
</script>
