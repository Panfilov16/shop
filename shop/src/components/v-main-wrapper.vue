<template>
    <div class="v-main-wrapper">
          vMainWrapper
    </div>
</template>

<script>
    export default {
       name: "v-main-wrapper",
       components: {},
       props: {},
       data(){
        return{
        title: "Gbpltw",
        }
       }, 
       computed: {},
       methods: {},
       watch: {},
       mounted (){
        console.log("mounted");
       }
    }
</script>

<style>
.v-main-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
    }
</style>