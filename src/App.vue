<template>
    <div>
        <Methods />
        <VModel />
    </div>
</template>

<script>
    import Methods from './components/Methods.vue';
    import VModel from './components/VModel.vue';
    export default {
        name:'App',
        components:{
            Methods,
            VModel,
        }
    }
</script>

<style scoped>

</style>