<template>
    <div>
        <h2>{{ name }}</h2>
    </div>
</template>

<script>
    import { ref } from 'vue';
    export default {
        name:'DemoOne',
        setup(){
            const name = ref('Reyansh')

            setTimeout(() =>{
                name.value = 'Goutham'
                console.log(name);
            },2000)
            return{
                name
            }
        }
        
    }
</script>

<style scoped>

</style>