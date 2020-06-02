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
    flex: 1 0 250px;
    margin: 0 20px 20px 0;

    .element-content{
        opacity: 0.7;
        height: 100%;

        .heading{
            text-align: center;
            line-height: 40px;
            background-color: black;
            color: white;
            margin: 0;
        }
    }
}
</style>

<script>
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