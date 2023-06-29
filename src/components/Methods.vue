<template>
    <div>
        <h2> {{ name }} </h2>
        <button @click="setName">Change Name</button>
        <h2>{{count}}</h2>
        <button @click="incrementCount">Increment Count</button>

        <h2>{{first}} {{last}}</h2>
        <button @click="changeHero">Change Hero</button>
    </div>
</template>

<script>
    import { ref, reactive, toRefs } from 'vue';
    export default {
        name: 'Methods',
        setup(){
            const count = ref(0)

            function incrementCount(){
                count.value++
            }

            const state = reactive({
                first: 'Naresh',
                last: 'Eluru',
            })

            function changeHero(){
                state.first = 'surya'
                state.last = 'vamshi'
            }
            return{
                count,
                incrementCount,
                ...toRefs(state),
                changeHero,
            }
        },
        data(){
            return{
                name: 'Rajesh',
            }
        },
        methods: {
            setName(){
                this.name = 'Vinod'
            }
        },
    }
</script>

<style scoped>

</style>