<template>
    <div>
        <DemoOne />
        <DemoTwo />
    </div>
</template>

<script>
    import DemoOne from './components/DemoOne.vue';
    import DemoTwo from './components/DemoTwo.vue';
    export default {
        name:'App',
        components:{
            DemoOne,
            DemoTwo
        }
    }
</script>

<style scoped>

</style>