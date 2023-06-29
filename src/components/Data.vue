<template>
    <div>
        <h2>Options - {{o_firstName}}</h2>
        <h2>Options - {{o_firstName}} {{o_lastName}} a.k.a {{o_heroName}}</h2>
        <h2>Composition - {{c_firstName}}</h2>
        <h2>Composition - {{greet}}</h2>
        <h2>Composition - {{c_firstName}} {{c_lastName}} {{c_heroName}}</h2>
        <h2>Composition - {{ greetHero }}</h2>

        <h2>{{state.firstName}} {{state.lastName}} {{state.heroName}}</h2>
        <h2>Composition - {{reactiveGreetHero}}</h2>
    </div>
</template>

<script>
    import { ref,reactive } from 'vue';
    export default {
        name:'Data',
        setup(){
            const c_firstName = ref('Prasad')
            const c_lastName = ref('Prasad1')
            const c_herotName = ref('Ram')
            // c_firstName.value='Rajender'
            const greet = `Hello ${c_firstName.value}`
            const greetHero = `Hello ${c_firstName.value} ${c_lastName.value} ${c_herotName.value}`
            console.log("c_firstName",c_firstName);

            const state = reactive({
                firstName: 'Vijay',
                lastName: 'Arun',
                heroName: 'Mahesh',
            })

            const reactiveGreetHero = `Hello ${state.firstName} ${state.lastName} a.k.a ${state.heroName}`
            return{
                c_firstName,
                greet,
                greetHero,
                state,
                reactiveGreetHero,
            }
        },
        data(){
            return{
                o_firstName: 'Rajendra',
                o_lastName: 'raj',
                o_heroName: 'charan',
            }
        },
    }
</script>

<style scoped>

</style>