<template>
    <div>
        <h2>{{firstName}} {{lastName}}</h2>
    </div>
</template>

<script>
    import { reactive, toRefs } from 'vue';
    export default {
        name:'DemoTwo',
        setup(){
            const state = reactive({
                firstName: 'John',
                lastName: 'Cena',
            })
            setTimeout(() =>{
                state.firstName = 'Jonny',
                state.lastName = 'Bairstaw',
                console.log(state);
            },2000)
            return toRefs(state)
                // firstName: state.firstName,
                // lastName: state.lastName,
        }
    }
</script>

<style scoped>

</style>