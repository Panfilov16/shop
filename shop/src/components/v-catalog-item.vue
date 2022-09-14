<template>
    <div class="v-catalog-item">
     <img class="v-catalog-item__image" :src="require('../assets/images/'+product_data.image)" alt="img">
     <p class="v-catalog-item-name">Name: {{product_data.name}}</p>
     <p class="v-catalog-item-price">Price:{{product_data.price}} р.</p>
     <button 
          class="v-catalog-item_add_to_cart_btn btn" 
          @click="sendDataToParent">
          Add to card
     </button>
    </div>
</template>

<script>
    export default {
        name: "v-catalog-item",
        props:{
          product_data: {
            type: Object,
            default(){
                return {}
            }
          }
        },
        data(){
            return {}
        },
        computed: {},
        methods: {
            sendDataToParent (){
                this.$emit( Event('sendArticle', this.product_data.article))
            }
        }
    }
</script>

<style>
.v-catalog-item {
    flex-basis: 25%;
    box-shadow: 0 0 8px 0 #e0e0e0;
    padding: 16px;
    margin-bottom: 16px;
}
.v-catalog-item__image {
    width: 100px;
}
</style>