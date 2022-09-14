<template>
    <div class="App">
  
      <v-main-wrapper/>
    </div>
</template>

<script>
   import vMainWrapper from "./components/v-main-wrapper.vue"
    export default {
        name: 'App',
        components: {
            vMainWrapper
        }
        
    }
</script>

<style>
.App {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 900px;
    margin: 0 auto;
}
    
</style>