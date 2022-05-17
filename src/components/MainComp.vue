<template>
  <main>
      <div class="container card-container"  v-if="isLoaded">
          <CardComp
         
          v-for="(item ,index) in arrCards"
          :key="`item-${index}`"
          :cardItem="item"
          
          />
          
      </div>
      <div class="container loader-container" v-else>
          <LoaderComp />
      </div>
      
  </main>
</template>

<script>
import axios from "axios";
import CardComp from './CardComp.vue';
import LoaderComp from "./LoaderComp.vue";

export default {
    name: "MainComp",

    data(){
        return{
            baseURL:"https://flynn.boolean.careers/exercises/api/array/music",
            arrCards :[],
            isLoaded : false,
        }
    },

    components: { CardComp, LoaderComp },

    mounted(){
        this.getAPI()
    },

    methods:{
        getAPI(){
            axios.get(this.baseURL)
            .then(res =>{
                this.arrCards = res.data.response;
                this.isLoaded= true;
                

            })

        }
    }
}
</script>

<style lang="scss" scoped>
main{
    
    width: 100%;
    height:100vh;
    background-color:#1e2d3b ;
    .card-container{
        
        padding: 20px;
        display: flex;
        flex-wrap: wrap;
        
        
    }
    .loader-container{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
}


</style>