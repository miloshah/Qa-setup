<template>
  <div id="app">
    <div class="page_wrapper">
      <MockPage></MockPage>
    </div>
  </div>
</template>

<style lang="scss">
  body{
    margin: 0;
  }
  input{
    text-align:center;
  }
  input:focus::placeholder {
    color: transparent;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;

    .page_wrapper{
      max-width: 1500px;
      width: 100%;
      margin: 0 auto;
    }
}
</style>

<script>
import MockPage from "@/views/MockPage.vue";

export default {
  name: "Home",
  components: {
    MockPage
  },
};
</script>