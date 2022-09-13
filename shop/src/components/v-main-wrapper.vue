<template>
    <div class="v-main-wrapper">
          vMainWrapper
          <v-catalog/>
          <v-cart/>
    </div>
</template>

<script>
    import vCatalog from "./v-catalog.vue"
    import vCart from "./v-cart.vue"
    export default {
       name: "v-main-wrapper",
       components: {
        vCatalog,
        vCart,
       },
       props: {},
       data(){
        return{
        title: "main-wrapper",
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
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
    }
</style>