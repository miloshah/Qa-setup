<template>
    <div class="web-elem-wrapper">
        <div class="element-content"
            @mouseover="hover = true"
            @mouseleave="hover = false"
            :class="{ active: hover}"
            :style="[backgroundImg]"
            >
         <h2 class="heading">{{elemdata.title}}</h2>
        </div>
    </div>
</template>

<style lang="scss">
.active{
    opacity: 1 !important;
}
.web-elem-wrapper{
    height: 300px;
    flex: 1;
    margin: 0 20px;

    @media screen and (max-width: 1000px){
        margin: 0 10px;
    }

    @media screen and (max-width: 700px){ 
        height: 200px;
    }
    
    @media screen and (max-width: 400px){
        margin: 0 5px;
        height: 150px;
    }

    .element-content{
        opacity: 0.7;
        height: 100%;
        // background: url("../assets/1.jpg") no-repeat;
        // background-color: #efefef;
        background-size: cover;
        // background-position: 50%;

        .heading{
            text-align: center;
            line-height: 40px;
            background-color: black;
            color: white;
            margin: 0;

            @media screen and (max-width: 500px ){
                line-height: 1;
                font-size: 15px;
            }
        }
    }
}

</style>

<script>
// @import "../assets/"
export default {
    name:"WebElements",
    data: function(){
        return{
            hover: false,
            backgroundImg:{
                background: 'url(' + require('../assets/'+this.elemdata.imgPath) + ')',
                backgroundRepeat: 'no-repeat',
                backgroundColor: '#efefef',
                backgroundSize: 'cover',
                backgroundPosition: '50%'
            }
        }
    },
    props: ['elemdata'],
}
</script>