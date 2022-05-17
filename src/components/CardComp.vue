<template>
  <div class="box">
      <img :src="cardItem.poster" alt="">
      <span class="title">{{cardItem.title}}</span>
      <span class="author">{{cardItem.author}}</span>
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
    width: calc(100%/6);
    background-color: #2e3a46;
    margin: 20px;
    padding: 15px;
    img{
        width: 100%;
    }
}

</style>