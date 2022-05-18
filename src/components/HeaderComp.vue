<template>
  <header>
    <img src="https://icones.pro/wp-content/uploads/2021/04/logo-spotify-icone-original.png" alt="logo">
    <div class="custom-select" >
  <select
    v-model="selected"
   @change="$emit('search',selected )">
    <option disabled value="" >Seleziona un genere:</option>
    
    <option >Rock</option>
    <option>jazz</option>
    <option >Pop</option>
    <option >Metal</option>
  </select>
</div>
    
  </header>
</template>

<script>
export default {
    name:"HeaderComp",
    data(){
      return{
         selected:""

      }
    }

}
</script>

<style lang="scss" scoped>
  header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 100px;
    background-color: #283038;
    img{
      width: 80px;
      padding: 15px;
    }
  }
  .custom-select{
    padding: 15px;
    select{
      width: 200px;
      height: 40px;
    }
  }


</style>