<template>
    <div class="page-header">
      <div class="logo-container">
        <a href="" @click="stopClick"></a>
      </div>
      <form class="search-container"
      :class="{ scroll: isIphone}"
      v-on:submit.prevent
      >
        <input type="text" class="searchTerm" placeholder="What are you looking for?">
        <button type="submit" class="searchButton">search</button>      
      </form>   
    </div>
</template>

<style lang="scss">
.scroll{
       margin-left: 50px !important;
    }

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

      @media screen and (max-width: 450px){
        padding: 0 5px 0 0;
        flex:0 0 80px;
      }
      
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

    @media screen and (max-width: 800px){ 
        margin-left: 0;
    }
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

    @media screen and (max-width: 500px){ 
      flex: 1;
    }
  }

  .scroll{
    .searchTerm{
      @media screen and (max-width: 500px){ 
        flex: 0 0 80%;
      } 
    }

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

    @media screen and (max-width: 500px){ 
      flex: 0 0 100px;
    }

    
    @media screen and (max-width: 400px){ 
      flex: 0 0 50px;
      font-size: 12px;
    }
  }

}
</style>

<script>

export default {
  name: "Header",
  computed: {
    isIphone: function(){
      var ios =   /iPhone/.test(navigator.userAgent) && 
                !window.MSStream;
      console.log(ios);
      return ios;
    }
  },
  methods:{
    stopClick(event){
      event.preventDefault();
    }
  }
};
</script>
