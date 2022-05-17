<template>
  <main>
      <div class="container card-container">
          <CardComp
          v-for="(item ,index) in arrCards"
          :key="`item-${index}`"
          :cardItem="item"
          
          />
      </div>
  </main>
</template>

<script>
import axios from "axios";
import CardComp from './CardComp.vue';

export default {
    name: "MainComp",

    data(){
        return{
            baseURL:"https://flynn.boolean.careers/exercises/api/array/music",
            arrCards :[],
        }
    },

    components: { CardComp },

    mounted(){
        this.getAPI()
    },

    methods:{
        getAPI(){
            axios.get(this.baseURL)
            .then(res =>{
                this.arrCards = res.data.response;
                

            })

        }
    }
}
</script>

<style lang="scss" scoped>
main{
    
    width: 100%;
    height:calc(100vh - 100px);
    background-color:#1e2d3b ;
    .card-container{
        padding: 20px;
        display: flex;
        
        flex-wrap: wrap;
        
    }
}


</style>