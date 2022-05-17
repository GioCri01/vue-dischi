<template>
  <header>
    <img src="https://icones.pro/wp-content/uploads/2021/04/logo-spotify-icone-original.png" alt="logo">
    <div class="custom-select" >
  <select>
    <option value="0">Seleziona un genere:</option>
    <option value="1">Rock</option>
    <option value="2">blues</option>
    <option value="3">Pop</option>
  </select>
</div>
    
  </header>
</template>

<script>
export default {
    name:"HeaderComp",

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