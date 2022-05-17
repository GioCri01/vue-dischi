<template>
  <div class="box">
      
      <img :src="cardItem.poster" alt="">
      <span class="title">{{cardItem.title}}</span>
      <span class="author">{{cardItem.author}}</span>
      <span class="year">{{cardItem.year}}</span>
        </div>
  
      
    
      
      
  
  
</template>

<script>

export default {
    name:"CardComp",
   

    props:{
        cardItem: Object
    }

    

}
</script>

<style lang="scss" scoped>
.box{
    width: calc(100%/5 - 40px);
    border-radius: 10px ;
    background-color: #2e3a46;
    margin: 20px;
    padding: 15px;
    text-align: center;
    transition: all 0.3s;
    &:hover{
        transform: scale(1.2);
        cursor: pointer;
    }
    img{
        width: 100%;
    }
    
    .author,
    .year{
        display: block;
        padding: 5px 0;
        font-size: 20px;
        color: gray;
    }

    .title{
        display: block;
        padding: 10px 0;
        font-size: 20px;
        color: white;

    }
}

</style>