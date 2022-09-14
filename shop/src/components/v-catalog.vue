<template>
    <div class="v-catalog">
     <h1>Catalog</h1>
     <v-catalog-item
     v-for="product in products"
     :key="product.article"
     :product_data="product"
    @sendArticle="showChildArticleInConsole"
     />
    </div>
</template>

<script>
    import vCatalogItem from "./v-catalog-item.vue"
    export default {
        name: 'v-catalog',
        components: {
            vCatalogItem,
        },
        props: {},
        data(){
            return{
                products:[
                    {
                     image: "1.jpg",
                     name: "T-shirt 1",
                     price: 100,
                     article: "T1",
                     available: true,
                    },
                    {
                     image: "2.jpg",
                     name: "T-shirt 2",
                     price: 150,
                     article: "T2",
                     available: true,
                    },
                     {
                     image: "3.jpg",
                     name: "T-shirt 3",
                     price: 200,
                     article: "T3",
                     available: false,
                    }
                ]
            }
        },
        computed: {},   
        methods: {
            showChildArticleInConsole (data){
                console.log(data)
            }
        }
    }
</script>

<style>
.v-catalog {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
}
</style>