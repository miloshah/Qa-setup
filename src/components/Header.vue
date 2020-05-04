<template>
    <div class="page-header">
      <div class="logo-container">
        <a href="#"></a>
      </div>
      <form class="search-container">
        <input type="text" class="searchTerm" placeholder="What are you looking for?">
        <button type="submit" class="searchButton">search</button>      
      </form>   
    </div>
</template>

<style lang="scss">
  .page-header{
    max-width: 100%;
    height: 80px;
    border-bottom: 2px solid rgba(0,0,0,.2);
    background-color: #fff;
    padding: 0 20px;
    display: flex;
    align-items: center;

  .logo-container{
      height: 50px;
      flex:0 0 100px;
      padding: 0 20px;
      
      a {
        background: url("../assets/mnet_logo.jpg") no-repeat;
        background-size: contain;
        height: 100%;
        display: block;
        margin: 0 auto;
      }
  }

  .search-container{
     display: flex;
     max-width: 800px;
    /* width: 100%; */
    flex: 1 1 auto;
    margin-left: 150px;
  }

  .searchTerm {
    // width: 100%;
    flex: 0 0 80%;
    border: 3px solid #00B4CC;
    border-right: none;
    padding: 5px;
    height: 20px;
    border-radius: 5px 0 0 5px;
    outline: none;
    color: #9DBFAF;
  }

  .searchTerm:focus{
  color: #00B4CC;
  }

  .searchButton {
    width: 100%;
    height: 36px;
    border: 1px solid #00B4CC;
    background: #00B4CC;
    text-align: center;
    color: #fff;
    border-radius: 0 5px 5px 0;
    cursor: pointer;
    font-size: 20px;
  }

}
</style>

<script>

export default {
  name: "Header"
};
</script>
