<template>
  <div id="app">
    <div class="page_wrapper">
      <MockPage></MockPage>
    </div>
  </div>
</template>

<style lang="scss">
  a, a:hover, a:focus, a:active {
      text-decoration: none;
  }
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
  created: function () {
    this.browserDetection();
  },
  methods:{
    browserDetection(){
      // Get the user-agent string 
            let userAgentString =  
                navigator.userAgent; 
          
            // Detect Chrome 
            window.isChrome =  
                userAgentString.indexOf("Chrome") > -1; 
          
            // Detect Internet Explorer 
            window.isIE =  
                userAgentString.indexOf("MSIE") > -1 ||  
                userAgentString.indexOf("rv:") > -1; 
          
            // Detect Firefox 
            window.isFireFox =  
                userAgentString.indexOf("Firefox") > -1; 
          
            // Detect Safari 
            window.isSafari =  
                userAgentString.indexOf("Safari") > -1; 
                  
            // Discard Safari since it also matches Chrome 
            if ((window.isChrome) && (window.isSafari))  
                window.isSafari = false; 
          
            // Detect Opera 
            window.isOpera =  
                userAgentString.indexOf("OP") > -1; 
                  
            // Discard Chrome since it also matches Opera      
            if ((window.isChrome) && (window.isOpera))  
                window.isChrome = false;
    }

  }
};
</script>